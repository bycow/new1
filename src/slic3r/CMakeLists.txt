cmake_minimum_required(VERSION 3.13)
project(libslic3r_gui)

include(PrecompiledHeader)

set(SLIC3R_GUI_SOURCES
    pchheader.cpp
    pchheader.hpp
    GUI/Printer/PrinterFileSystem.cpp
    GUI/Printer/PrinterFileSystem.h
    GUI/Widgets/AxisCtrlButton.cpp
    GUI/Widgets/AxisCtrlButton.hpp
    GUI/Widgets/Button.cpp
    GUI/Widgets/Button.hpp
    GUI/Widgets/CheckBox.cpp
    GUI/Widgets/CheckBox.hpp
    GUI/Widgets/RadioBox.hpp
    GUI/Widgets/RadioBox.cpp
    GUI/Widgets/ProgressDialog.hpp
    GUI/Widgets/ProgressDialog.cpp
    GUI/Widgets/RoundedRectangle.hpp
    GUI/Widgets/RoundedRectangle.cpp
    GUI/Widgets/ComboBox.cpp
    GUI/Widgets/ComboBox.hpp
    GUI/Widgets/SideButton.hpp
    GUI/Widgets/SideButton.cpp
    GUI/Widgets/SideMenuPopup.hpp
    GUI/Widgets/SideMenuPopup.cpp
    GUI/Widgets/DropDown.cpp
    GUI/Widgets/DropDown.hpp
    GUI/Widgets/Label.cpp
    GUI/Widgets/Label.hpp
    GUI/Widgets/Scrollbar.cpp
    GUI/Widgets/Scrollbar.hpp
    GUI/Widgets/ScrolledWindow.cpp
    GUI/Widgets/ScrolledWindow.hpp
    GUI/Widgets/StaticBox.cpp
    GUI/Widgets/StaticBox.hpp
    GUI/Widgets/ImageSwitchButton.cpp
    GUI/Widgets/ImageSwitchButton.hpp
    GUI/Widgets/SwitchButton.cpp
    GUI/Widgets/SwitchButton.hpp
    GUI/Widgets/SpinInput.cpp
    GUI/Widgets/SpinInput.hpp
    GUI/Widgets/StaticLine.cpp
    GUI/Widgets/StaticLine.hpp
    GUI/Widgets/StateColor.cpp
    GUI/Widgets/StateColor.hpp
    GUI/Widgets/StateHandler.cpp
    GUI/Widgets/StateHandler.hpp
    GUI/Widgets/TabCtrl.cpp
    GUI/Widgets/TabCtrl.hpp
    GUI/Widgets/TextInput.cpp
    GUI/Widgets/TextInput.hpp
    GUI/Widgets/TempInput.cpp
    GUI/Widgets/TempInput.hpp
    GUI/Widgets/AMSControl.cpp
    GUI/Widgets/AMSControl.hpp
    GUI/Widgets/Scrollbar.cpp
    GUI/Widgets/Scrollbar.hpp
    GUI/Widgets/ScrolledWindow.cpp
    GUI/Widgets/ScrolledWindow.hpp
    GUI/Widgets/StepCtrl.cpp
    GUI/Widgets/StepCtrl.hpp
    GUI/Widgets/ProgressBar.cpp
    GUI/Widgets/ProgressBar.hpp
    GUI/Widgets/SideTools.cpp
    GUI/Widgets/SideTools.hpp
    GUI/Widgets/WebView.cpp
    GUI/Widgets/WebView.hpp
    GUI/AboutDialog.cpp
    GUI/AboutDialog.hpp
    GUI/AuxiliaryDialog.cpp
    GUI/AuxiliaryDialog.hpp
    GUI/Auxiliary.cpp
    GUI/Auxiliary.hpp
    GUI/BackgroundSlicingProcess.cpp
    GUI/BackgroundSlicingProcess.hpp
    GUI/BitmapCache.cpp
    GUI/BitmapCache.hpp
    GUI/ImageGrid.cpp
    GUI/ImageGrid.h
    GUI/3DScene.cpp
    GUI/3DScene.hpp
    GUI/format.hpp
    GUI/GLShadersManager.hpp
    GUI/GLShadersManager.cpp
    GUI/GLShader.cpp
    GUI/GLShader.hpp
    GUI/GLCanvas3D.hpp
    GUI/GLCanvas3D.cpp
    GUI/OpenGLManager.hpp
    GUI/OpenGLManager.cpp
    GUI/Selection.hpp
    GUI/Selection.cpp
    GUI/Gizmos/GLGizmosManager.cpp
    GUI/Gizmos/GLGizmosManager.hpp
    GUI/Gizmos/GLGizmosCommon.cpp
    GUI/Gizmos/GLGizmosCommon.hpp
    GUI/Gizmos/GLGizmoBase.cpp
    GUI/Gizmos/GLGizmoBase.hpp
    GUI/Gizmos/GLGizmoMove.cpp
    GUI/Gizmos/GLGizmoMove.hpp
    GUI/Gizmos/GLGizmoRotate.cpp
    GUI/Gizmos/GLGizmoRotate.hpp
    GUI/Gizmos/GLGizmoScale.cpp
    GUI/Gizmos/GLGizmoScale.hpp
    GUI/Gizmos/GLGizmoSlaSupports.cpp
    GUI/Gizmos/GLGizmoSlaSupports.hpp
    GUI/Gizmos/GLGizmoFdmSupports.cpp
    GUI/Gizmos/GLGizmoFdmSupports.hpp
    GUI/Gizmos/GLGizmoFlatten.cpp
    GUI/Gizmos/GLGizmoFlatten.hpp
    GUI/Gizmos/GLGizmoAdvancedCut.cpp
    GUI/Gizmos/GLGizmoAdvancedCut.hpp
    GUI/Gizmos/GLGizmoHollow.cpp
    GUI/Gizmos/GLGizmoHollow.hpp
    GUI/Gizmos/GLGizmoPainterBase.cpp
    GUI/Gizmos/GLGizmoPainterBase.hpp
    GUI/Gizmos/GLGizmoSimplify.cpp
    GUI/Gizmos/GLGizmoSimplify.hpp
    GUI/Gizmos/GLGizmoMmuSegmentation.cpp
    GUI/Gizmos/GLGizmoMmuSegmentation.hpp
    GUI/Gizmos/GLGizmoFaceDetector.cpp
    GUI/Gizmos/GLGizmoFaceDetector.hpp
    GUI/Gizmos/GLGizmoSeam.cpp
    GUI/Gizmos/GLGizmoSeam.hpp
    GUI/Gizmos/GLGizmoModifier.cpp
    GUI/Gizmos/GLGizmoModifier.hpp
    GUI/GLSelectionRectangle.cpp
    GUI/GLSelectionRectangle.hpp
    GUI/Gizmos/GizmoObjectManipulation.cpp
    GUI/Gizmos/GizmoObjectManipulation.hpp
    GUI/GLModel.hpp
    GUI/GLModel.cpp
    GUI/GLTexture.hpp
    GUI/GLTexture.cpp
    GUI/GLToolbar.hpp
    GUI/GLToolbar.cpp
    GUI/IMToolbar.hpp
    GUI/IMToolbar.cpp
    GUI/GCodeViewer.hpp
    GUI/GCodeViewer.cpp
    GUI/Preferences.cpp
    GUI/Preferences.hpp
    GUI/AMSSetting.cpp
    GUI/AMSSetting.hpp
    GUI/AMSMaterialsSetting.cpp
    GUI/AMSMaterialsSetting.hpp
    GUI/PresetHints.cpp
    GUI/PresetHints.hpp
    GUI/GUI.cpp
    GUI/GUI.hpp
    GUI/GUI_Init.cpp
    GUI/GUI_Init.hpp
    GUI/GUI_Preview.cpp
    GUI/GUI_Preview.hpp
    GUI/GUI_App.cpp
    GUI/GUI_App.hpp
    GUI/GUI_Utils.cpp
    GUI/GUI_Utils.hpp
    GUI/I18N.cpp
    GUI/I18N.hpp
    GUI/MainFrame.cpp
    GUI/MainFrame.hpp
    GUI/BBLTopbar.cpp
    GUI/BBLTopbar.hpp
    GUI/Plater.cpp
    GUI/Plater.hpp
    GUI/PartPlate.cpp
    GUI/PartPlate.hpp
    GUI/PresetComboBoxes.hpp
    GUI/PresetComboBoxes.cpp
    GUI/BitmapComboBox.hpp
    GUI/BitmapComboBox.cpp
    GUI/SavePresetDialog.hpp
    GUI/SavePresetDialog.cpp
    GUI/GUI_Colors.hpp
    GUI/GUI_Colors.cpp
    GUI/GUI_Factories.cpp
    GUI/GUI_Factories.hpp
    GUI/GUI_ObjectList.cpp
    GUI/GUI_ObjectList.hpp
    GUI/GUI_AuxiliaryList.cpp
    GUI/GUI_AuxiliaryList.hpp
    GUI/GUI_ObjectSettings.cpp
    GUI/GUI_ObjectSettings.hpp
    GUI/GUI_ObjectTable.cpp
    GUI/GUI_ObjectTable.hpp
    GUI/GUI_ObjectTableSettings.cpp
    GUI/GUI_ObjectTableSettings.hpp
    GUI/MeshUtils.cpp
    GUI/MeshUtils.hpp
    GUI/Tab.cpp
    GUI/Tab.hpp
    GUI/ParamsDialog.cpp
    GUI/ParamsDialog.hpp
    GUI/ParamsPanel.cpp
    GUI/ParamsPanel.hpp
    GUI/AmsWidgets.cpp
    GUI/AmsWidgets.hpp
    GUI/MediaFilePanel.cpp
    GUI/MediaFilePanel.h
    GUI/MediaPlayCtrl.cpp
    GUI/MediaPlayCtrl.h
    GUI/MonitorBasePanel.cpp
    GUI/MonitorBasePanel.h
    GUI/UpgradePanel.cpp
    GUI/UpgradePanel.hpp
    GUI/HMSPanel.hpp
    GUI/HMSPanel.cpp
    GUI/MonitorPage.cpp
    GUI/MonitorPage.hpp
    GUI/StatusPanel.cpp
    GUI/StatusPanel.hpp
    GUI/SliceInfoPanel.cpp
    GUI/SliceInfoPanel.hpp
    GUI/CameraPopup.cpp
    GUI/CameraPopup.hpp
    GUI/Monitor.cpp
    GUI/Monitor.hpp
    GUI/WebViewDialog.cpp
    GUI/WebViewDialog.hpp
    GUI/WebDailytipDialog.hpp
    GUI/WebDailytipDialog.cpp
    GUI/WebGuideDialog.hpp
    GUI/WebGuideDialog.cpp
    GUI/WebUserLoginDialog.cpp
    GUI/WebUserLoginDialog.hpp
    GUI/ConfigManipulation.cpp
    GUI/ConfigManipulation.hpp
    GUI/Field.cpp
    GUI/Field.hpp
    GUI/OptionsGroup.cpp
    GUI/OptionsGroup.hpp
    GUI/OG_CustomCtrl.cpp
    GUI/OG_CustomCtrl.hpp
    GUI/MarkdownTip.cpp
    GUI/MarkdownTip.hpp
    GUI/2DBed.cpp
    GUI/2DBed.hpp
    GUI/3DBed.cpp
    GUI/3DBed.hpp
    GUI/Camera.cpp
    GUI/Camera.hpp
    GUI/wxExtensions.cpp
    GUI/wxExtensions.hpp
    GUI/WipeTowerDialog.cpp
    GUI/WipeTowerDialog.hpp
    #GUI/RemovableDriveManager.cpp
    #GUI/RemovableDriveManager.hpp
    GUI/SendSystemInfoDialog.cpp
    GUI/SendSystemInfoDialog.hpp
    GUI/ImGuiWrapper.hpp
    GUI/ImGuiWrapper.cpp
    GUI/DeviceManager.hpp
    GUI/DeviceManager.cpp
    Config/Snapshot.cpp
    Config/Snapshot.hpp
    Config/Version.cpp
    Config/Version.hpp
    Utils/ASCIIFolding.cpp
    Utils/ASCIIFolding.hpp
    GUI/ConfigWizard.cpp
    GUI/ConfigWizard.hpp
    GUI/ConnectPrinter.cpp
    GUI/ConnectPrinter.hpp
    GUI/ConfigWizard_private.hpp
    GUI/MsgDialog.cpp
    GUI/MsgDialog.hpp
    GUI/UpdateDialogs.cpp
    GUI/UpdateDialogs.hpp
    GUI/Jobs/Job.hpp
    GUI/Jobs/Job.cpp
    GUI/Jobs/PlaterJob.hpp
    GUI/Jobs/PlaterJob.cpp
    GUI/Jobs/ArrangeJob.hpp
    GUI/Jobs/ArrangeJob.cpp
    GUI/Jobs/OrientJob.hpp
    GUI/Jobs/OrientJob.cpp
    GUI/Jobs/RotoptimizeJob.hpp
    GUI/Jobs/RotoptimizeJob.cpp
    GUI/Jobs/FillBedJob.hpp
    GUI/Jobs/FillBedJob.cpp
    GUI/Jobs/SLAImportJob.hpp
    GUI/Jobs/SLAImportJob.cpp
    GUI/Jobs/ProgressIndicator.hpp
    GUI/Jobs/PrintJob.hpp
    GUI/Jobs/PrintJob.cpp
    GUI/Jobs/BindJob.hpp
    GUI/Jobs/BindJob.cpp
    GUI/Jobs/NotificationProgressIndicator.hpp
    GUI/Jobs/NotificationProgressIndicator.cpp
    GUI/ProgressStatusBar.hpp
    GUI/ProgressStatusBar.cpp
    GUI/BBLStatusBar.hpp
    GUI/BBLStatusBar.cpp
    GUI/BBLStatusBarSend.hpp
    GUI/BBLStatusBarSend.cpp
    GUI/BBLStatusBarBind.hpp
    GUI/BBLStatusBarBind.cpp
    GUI/Mouse3DController.cpp
    GUI/Mouse3DController.hpp
    GUI/IMSlider.cpp
    GUI/IMSlider.hpp
    GUI/IMSlider_Utils.hpp
    GUI/Notebook.cpp
    GUI/Notebook.hpp
    GUI/TabButton.cpp
    GUI/TabButton.hpp
    GUI/Tabbook.cpp
    GUI/Tabbook.hpp
    GUI/ObjectDataViewModel.cpp
    GUI/ObjectDataViewModel.hpp
    GUI/AuxiliaryDataViewModel.cpp
    GUI/AuxiliaryDataViewModel.hpp
    #GUI/InstanceCheck.cpp
    #GUI/InstanceCheck.hpp
    GUI/Search.cpp
    GUI/Search.hpp
    GUI/NotificationManager.cpp
    GUI/NotificationManager.hpp
    GUI/UnsavedChangesDialog.cpp
    GUI/UnsavedChangesDialog.hpp
    GUI/ExtraRenderers.cpp
    GUI/ExtraRenderers.hpp
    GUI/ProjectDirtyStateManager.hpp
    GUI/ProjectDirtyStateManager.cpp
    GUI/DesktopIntegrationDialog.cpp
    GUI/DesktopIntegrationDialog.hpp
    GUI/PublishDialog.cpp
    GUI/PublishDialog.hpp
    GUI/BindDialog.cpp
    GUI/BindDialog.hpp
    GUI/SelectMachine.hpp
    GUI/SelectMachine.cpp
    GUI/AmsMappingPopup.hpp
    GUI/AmsMappingPopup.cpp
    GUI/ReleaseNote.hpp
    GUI/ReleaseNote.cpp
    GUI/Calibration.hpp
    GUI/Calibration.cpp
    Utils/json_diff.hpp
    Utils/json_diff.cpp
    GUI/KBShortcutsDialog.hpp
    GUI/KBShortcutsDialog.cpp
    Utils/Http.cpp
    Utils/Http.hpp
    Utils/FixModelByWin10.cpp
    Utils/FixModelByWin10.hpp
    Utils/Bonjour.cpp
    Utils/Bonjour.hpp
    Utils/PresetUpdater.cpp
    Utils/PresetUpdater.hpp
    Utils/Process.cpp
    Utils/Process.hpp
    Utils/Profile.hpp
    Utils/UndoRedo.cpp
    Utils/UndoRedo.hpp
    Utils/HexFile.cpp
    Utils/HexFile.hpp
    Utils/TCPConsole.cpp
    Utils/TCPConsole.hpp
    Utils/minilzo_extension.hpp
    Utils/minilzo_extension.cpp
    Utils/ColorSpaceConvert.hpp
    Utils/ColorSpaceConvert.cpp
    Utils/NetworkAgent.cpp
    Utils/NetworkAgent.hpp
)

if (APPLE)
    list(APPEND SLIC3R_GUI_SOURCES
            Utils/RetinaHelperImpl.mm
            Utils/MacDarkMode.mm
            #GUI/RemovableDriveManagerMM.mm
            #GUI/RemovableDriveManagerMM.h
            GUI/Mouse3DHandlerMac.mm
            #GUI/InstanceCheckMac.mm
            #GUI/InstanceCheckMac.h
            GUI/wxMediaCtrl2.mm
            GUI/wxMediaCtrl2.h
        )
    FIND_LIBRARY(DISKARBITRATION_LIBRARY DiskArbitration)
else ()
    list(APPEND SLIC3R_GUI_SOURCES
            GUI/wxMediaCtrl2.cpp
            GUI/wxMediaCtrl2.h
        )
endif ()

add_library(libslic3r_gui STATIC ${SLIC3R_GUI_SOURCES})
target_include_directories(libslic3r_gui PRIVATE Utils)

source_group(TREE ${CMAKE_CURRENT_SOURCE_DIR} FILES ${SLIC3R_GUI_SOURCES})

encoding_check(libslic3r_gui)

target_link_libraries(libslic3r_gui libslic3r cereal imgui minilzo GLEW::GLEW OpenGL::GL hidapi libcurl OpenSSL::SSL OpenSSL::Crypto
${wxWidgets_LIBRARIES} glfw)

if (MSVC)
    target_link_libraries(libslic3r_gui Setupapi.lib)
elseif (CMAKE_SYSTEM_NAME STREQUAL "Linux")
    target_link_libraries(libslic3r_gui ${DBUS_LIBRARIES} OSMesa)
elseif (APPLE)
    target_link_libraries(libslic3r_gui ${DISKARBITRATION_LIBRARY})
endif()

if (SLIC3R_STATIC)
    # FIXME: This was previously exported by wx-config but the wxWidgets
    # cmake build forgets this and the build fails in debug mode (or on raspberry release)
    target_compile_definitions(libslic3r_gui PUBLIC -DwxDEBUG_LEVEL=0)
endif()

if (SLIC3R_STATIC AND NOT SLIC3R_STATIC_EXCLUDE_CURL AND UNIX AND NOT APPLE)
    target_compile_definitions(libslic3r_gui PRIVATE OPENSSL_CERT_OVERRIDE)
endif ()

if (SLIC3R_PCH AND NOT SLIC3R_SYNTAXONLY)
    add_precompiled_header(libslic3r_gui pchheader.hpp FORCEINCLUDE)
endif ()

# We need to implement some hacks for wxWidgets and touch the underlying GTK
# layer and sub-libraries. This forces us to use the include locations and
# link these libraries.
if (UNIX AND NOT APPLE)
    find_package(GTK${SLIC3R_GTK} REQUIRED)
    target_include_directories(libslic3r_gui PRIVATE ${GTK${SLIC3R_GTK}_INCLUDE_DIRS})
    target_link_libraries(libslic3r_gui ${GTK${SLIC3R_GTK}_LIBRARIES})
endif ()
