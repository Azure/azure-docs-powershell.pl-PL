---
title: Instalowanie i konfigurowanie programu Azure PowerShell | Microsoft Docs
description: Jak zainstalować i skonfigurować program Azure PowerShell do pierwszego użycia.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.openlocfilehash: ef796bcb81e24b1942c644aad2b4ec7705916b02
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/05/2018
ms.locfileid: "52826548"
---
# <a name="install-and-configure-azure-powershell"></a><span data-ttu-id="f35ea-103">Instalowanie i konfigurowanie programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f35ea-103">Install and configure Azure PowerShell</span></span>

<span data-ttu-id="f35ea-104">W tym artykule opisano kroki instalowania modułów programu Azure PowerShell w środowisku systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="f35ea-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment.</span></span>
<span data-ttu-id="f35ea-105">Jeśli chcesz korzystać z programu Azure PowerShell w systemie macOS lub Linux, zobacz następujący artykuł: [Instalowanie i konfigurowanie programu Azure PowerShell w systemach macOS i Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="f35ea-105">If you want to use Azure PowerShell on macOS or Linux, see the following article: [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

<span data-ttu-id="f35ea-106">Instalowanie programu Azure PowerShell z Galerii programu PowerShell jest preferowaną metodą instalacji.</span><span class="sxs-lookup"><span data-stu-id="f35ea-106">Installing Azure PowerShell from the PowerShell Gallery is the preferred method of installation.</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="f35ea-107">Krok 1. Zainstaluj moduł PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="f35ea-107">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="f35ea-108">Instalowanie elementów z Galerii programu PowerShell wymaga modułu PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="f35ea-108">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="f35ea-109">Upewnij się, że masz odpowiednią wersję modułu PowerShellGet oraz spełnione inne wymagania systemowe.</span><span class="sxs-lookup"><span data-stu-id="f35ea-109">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="f35ea-110">Uruchom następujące polecenie, aby sprawdzić, czy w Twoim systemie został zainstalowany moduł PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="f35ea-110">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell-interactive
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="f35ea-111">Powinny zostać wyświetlone dane wyjściowe podobne do poniższych:</span><span class="sxs-lookup"><span data-stu-id="f35ea-111">You should see something similar to the following output:</span></span>

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="f35ea-112">Potrzebujesz programu PowerShellGet w wersji 1.1.2.0 lub nowszej.</span><span class="sxs-lookup"><span data-stu-id="f35ea-112">You need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="f35ea-113">Aby zaktualizować program PowerShellGet, użyj następującego polecenia:</span><span class="sxs-lookup"><span data-stu-id="f35ea-113">To update PowerShellGet, use the following command:</span></span>

```powershell-interactive
Install-Module PowerShellGet -Force
```

<span data-ttu-id="f35ea-114">Jeśli nie masz zainstalowanego modułu PowerShellGet, zobacz sekcję [Jak uzyskać moduł PowerShellGet](#how-to-get-powershellget) w niniejszym artykule.</span><span class="sxs-lookup"><span data-stu-id="f35ea-114">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget) section of this article.</span></span>

> [!NOTE]
> <span data-ttu-id="f35ea-115">Korzystanie z modułu PowerShellGet wymaga zasad wykonania pozwalających uruchamiać skrypty.</span><span class="sxs-lookup"><span data-stu-id="f35ea-115">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="f35ea-116">Aby uzyskać więcej informacji na temat zasad wykonania programu PowerShell, zobacz [Informacje o zasadach wykonania](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span><span class="sxs-lookup"><span data-stu-id="f35ea-116">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>
>
> [!IMPORTANT]
> <span data-ttu-id="f35ea-117">Moduł opisany w tym dokumencie (AzureRM) korzysta z programu .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="f35ea-117">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="f35ea-118">Dlatego jest on niezgodny z programem PowerShell 6.0, który korzysta z platformy .NET Core.</span><span class="sxs-lookup"><span data-stu-id="f35ea-118">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="f35ea-119">Jeśli korzystasz z programu PowerShell 6.0, postępuj zgodnie z [instrukcjami dotyczącymi instalacji dla systemów macOS i Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="f35ea-119">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="f35ea-120">Krok 2. Zainstaluj program Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f35ea-120">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="f35ea-121">Instalacja programu Azure PowerShell z Galerii programu PowerShell wymaga podniesionych uprawnień.</span><span class="sxs-lookup"><span data-stu-id="f35ea-121">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="f35ea-122">Uruchom następujące polecenie z sesji programu PowerShell z podwyższonym poziomem uprawnień:</span><span class="sxs-lookup"><span data-stu-id="f35ea-122">Run the following command from an elevated PowerShell session:</span></span>

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="f35ea-123">Galeria programu PowerShell domyślnie nie jest skonfigurowana jako zaufane repozytorium modułu PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="f35ea-123">By default, the PowerShell gallery is not configured as a Trusted repository for PowerShellGet.</span></span> <span data-ttu-id="f35ea-124">Po pierwszym użyciu Galerii programu PowerShell zostanie wyświetlony następujący komunikat:</span><span class="sxs-lookup"><span data-stu-id="f35ea-124">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

<span data-ttu-id="f35ea-125">Wybierz odpowiedź „Tak” lub „Tak na wszystkie”, aby kontynuować instalację.</span><span class="sxs-lookup"><span data-stu-id="f35ea-125">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="f35ea-126">Jeśli masz wersję pakietu NuGet starszą niż 2.8.5.201, zostanie wyświetlony monit o pobranie i zainstalowanie najnowszej wersji pakietu NuGet.</span><span class="sxs-lookup"><span data-stu-id="f35ea-126">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="f35ea-127">Moduł AzureRM to zbiorczy moduł poleceń cmdlet usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="f35ea-127">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="f35ea-128">Po zainstalowaniu modułu AzureRM każdy moduł programu Azure PowerShell, który nie został wcześniej zainstalowany, zostanie pobrany i zainstalowany z Galerii programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f35ea-128">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded and from the PowerShell Gallery.</span></span>

<span data-ttu-id="f35ea-129">Jeśli masz zainstalowaną poprzednią wersję programu Azure PowerShell, może wystąpić błąd.</span><span class="sxs-lookup"><span data-stu-id="f35ea-129">If you have a previous version of Azure PowerShell installed you may receive an error.</span></span> <span data-ttu-id="f35ea-130">Aby rozwiązać ten problem, zobacz [Aktualizowanie do nowej wersji programu Azure PowerShell](#update-azps) w dalszej części tego artykułu.</span><span class="sxs-lookup"><span data-stu-id="f35ea-130">To resolve this issue, see the [Updating to a new version of Azure PowerShell](#update-azps) section of this article.</span></span>

## <a name="step-3-load-the-azurerm-module"></a><span data-ttu-id="f35ea-131">Krok 3. Załaduj moduł AzureRM</span><span class="sxs-lookup"><span data-stu-id="f35ea-131">Step 3: Load the AzureRM module</span></span>

<span data-ttu-id="f35ea-132">Gdy moduł jest zainstalowany, musisz załadować moduł do swojej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f35ea-132">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="f35ea-133">Należy to zrobić w ramach normalnej sesji programu PowerShell (bez podwyższonego poziomu uprawnień).</span><span class="sxs-lookup"><span data-stu-id="f35ea-133">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="f35ea-134">Moduły są w następujący sposób ładowane przy użyciu polecenia cmdlet `Import-Module`:</span><span class="sxs-lookup"><span data-stu-id="f35ea-134">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell-interactive
Import-Module -Name AzureRM
```

## <a name="next-steps"></a><span data-ttu-id="f35ea-135">Następne kroki</span><span class="sxs-lookup"><span data-stu-id="f35ea-135">Next Steps</span></span>

<span data-ttu-id="f35ea-136">Aby uzyskać więcej informacji o korzystaniu z programu Azure PowerShell, zobacz następujące artykuły:</span><span class="sxs-lookup"><span data-stu-id="f35ea-136">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="f35ea-137">Rozpoczynanie pracy z programem Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f35ea-137">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="f35ea-138">Zgłaszanie problemów i przesyłanie opinii</span><span class="sxs-lookup"><span data-stu-id="f35ea-138">Reporting issues and feedback</span></span>

<span data-ttu-id="f35ea-139">Jeśli występują jakiekolwiek problemy związane z narzędziem, prześlij zgłoszenie do sekcji [Problemy](https://github.com/Azure/azure-powershell/issues) repozytorium GitHub.</span><span class="sxs-lookup"><span data-stu-id="f35ea-139">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-powershell/issues) section of our GitHub repo.</span></span> <span data-ttu-id="f35ea-140">Aby przekazać opinię z wiersza polecenia, użyj polecenia cmdlet `Send-Feedback`.</span><span class="sxs-lookup"><span data-stu-id="f35ea-140">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="f35ea-141">Często zadawane pytania</span><span class="sxs-lookup"><span data-stu-id="f35ea-141">Frequently asked questions</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="f35ea-142">Jak uzyskać moduł PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="f35ea-142">How to get PowerShellGet</span></span>

|<span data-ttu-id="f35ea-143">Wersja systemu operacyjnego</span><span class="sxs-lookup"><span data-stu-id="f35ea-143">OS Version</span></span>|<span data-ttu-id="f35ea-144">Instrukcje dotyczące instalacji</span><span class="sxs-lookup"><span data-stu-id="f35ea-144">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="f35ea-145">Mam system Windows 10 lub Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f35ea-145">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="f35ea-146">Wbudowane w platformę Windows Management Framework (WMF) 5.0 zawartą w systemie operacyjnym</span><span class="sxs-lookup"><span data-stu-id="f35ea-146">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="f35ea-147">Chcę przeprowadzić uaktualnienie do programu PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="f35ea-147">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="f35ea-148">Zainstaluj najnowszą wersję platformy WMF</span><span class="sxs-lookup"><span data-stu-id="f35ea-148">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|<span data-ttu-id="f35ea-149">Używam wersji systemu Windows mającej program PowerShell 3 lub 4</span><span class="sxs-lookup"><span data-stu-id="f35ea-149">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|[<span data-ttu-id="f35ea-150">Pobierz moduły PackageManagement</span><span class="sxs-lookup"><span data-stu-id="f35ea-150">Get the PackageManagement modules</span></span>](http://go.microsoft.com/fwlink/?LinkID=746217)|

### <a name="div-idhelpmechoosechecking-the-version-of-azure-powershell"></a><div id="helpmechoose"/><span data-ttu-id="f35ea-151">Sprawdzanie wersji programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f35ea-151">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="f35ea-152">Chociaż zachęcamy do jak najszybszego uaktualnienia do najnowszej wersji, różne wersje programu Azure PowerShell są nadal obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="f35ea-152">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="f35ea-153">Aby ustalić zainstalowaną wersję programu Azure PowerShell, uruchom polecenie `Get-Module AzureRM` z wiersza polecenia.</span><span class="sxs-lookup"><span data-stu-id="f35ea-153">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell-interactive
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a><span data-ttu-id="f35ea-154">Obsługa klasycznych metod wdrażania</span><span class="sxs-lookup"><span data-stu-id="f35ea-154">Support for classic deployment methods</span></span>

<span data-ttu-id="f35ea-155">Jeśli masz wdrożenia korzystające z klasycznego modelu wdrażania, możesz zainstalować wersję zarządzania usługą programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f35ea-155">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="f35ea-156">Aby uzyskać więcej informacji, zobacz [Instalowanie modułu Azure PowerShell Service Management](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="f35ea-156">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="f35ea-157">Moduły Azure i AzureRM mają wspólne zależności.</span><span class="sxs-lookup"><span data-stu-id="f35ea-157">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="f35ea-158">Jeśli korzystasz z modułów Azure i AzureRM, należy zainstalować tę samą wersję każdego pakietu.</span><span class="sxs-lookup"><span data-stu-id="f35ea-158">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a name="div-idupdate-azpsupdating-to-a-new-version-of-azure-powershell"></a><div id="update-azps"/><span data-ttu-id="f35ea-159">Uaktualnianie do nowej wersji programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f35ea-159">Updating to a new version of Azure PowerShell</span></span>

<span data-ttu-id="f35ea-160">Jeśli masz zainstalowaną poprzednią wersję programu Azure PowerShell obejmującą moduł zarządzania usługami, może wystąpić następujący błąd:</span><span class="sxs-lookup"><span data-stu-id="f35ea-160">If you have a previous version of Azure PowerShell installed that includes the Service Management module, you may receive the following error:</span></span>

```Output
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

<span data-ttu-id="f35ea-161">Zgodnie z treścią komunikatu o błędzie trzeba zainstalować moduł, podając parametr -AllowClobber.</span><span class="sxs-lookup"><span data-stu-id="f35ea-161">As the error message states, you need to use the -AllowClobber parameter to install the module.</span></span> <span data-ttu-id="f35ea-162">Użyj następującego polecenia:</span><span class="sxs-lookup"><span data-stu-id="f35ea-162">Use the following command:</span></span>

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="f35ea-163">Aby uzyskać więcej informacji, zobacz temat pomocy dotyczący parametru [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span><span class="sxs-lookup"><span data-stu-id="f35ea-163">For more information, see the help topic for [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span></span>

### <a name="installing-module-versions-side-by-side"></a><span data-ttu-id="f35ea-164">Instalowanie wersji modułu obok siebie</span><span class="sxs-lookup"><span data-stu-id="f35ea-164">Installing module versions side by side</span></span>

<span data-ttu-id="f35ea-165">Metoda instalacji PowerShellGet jest jedyną metodą, która obsługuje instalowanie wielu wersji.</span><span class="sxs-lookup"><span data-stu-id="f35ea-165">The PowerShellGet method of installation is the only method that supports the installation of multiple versions.</span></span> <span data-ttu-id="f35ea-166">Na przykład możesz mieć skrypty napisane przy użyciu poprzedniej wersji programu Azure PowerShell, do aktualizacji której nie masz czasu lub zasobów.</span><span class="sxs-lookup"><span data-stu-id="f35ea-166">For example, you may have scripts written using a previous version of Azure PowerShell that you don't have the time or resources to updated.</span></span> <span data-ttu-id="f35ea-167">Następujące polecenia przedstawiają sposób instalowania wielu wersji programu Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="f35ea-167">The following commands illustrate how to install multiple versions of Azure PowerShell:</span></span>

```powershell-interactive
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

<span data-ttu-id="f35ea-168">Tylko jedna wersja modułu może zostać załadowana w sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f35ea-168">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="f35ea-169">Musisz otworzyć nowe okno programu PowerShell i użyć polecenia `Import-Module`, aby zaimportować określoną wersję poleceń cmdlet modułu AzureRM:</span><span class="sxs-lookup"><span data-stu-id="f35ea-169">You must open a new PowerShell window and use `Import-Module` to import a specific version of the AzureRM cmdlets:</span></span>

```powershell-interactive
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

> [!NOTE]
> <span data-ttu-id="f35ea-170">Wersja 2.1.0 i wersja 1.2.6 to pierwsze wersje modułu przeznaczone do instalacji i używania obok siebie.</span><span class="sxs-lookup"><span data-stu-id="f35ea-170">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="f35ea-171">Załadowanie starszej wersji programu Azure PowerShell powoduje załadowanie niezgodnych wersji modułu **AzureRM.Profile**.</span><span class="sxs-lookup"><span data-stu-id="f35ea-171">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="f35ea-172">W wyniku tego każde wykonanie polecenia cmdlet powoduje wyświetlenie polecenia cmdlet z monitem o zalogowanie się.</span><span class="sxs-lookup"><span data-stu-id="f35ea-172">This results in the cmdlets prompting you to sign in whenever you execute a cmdlet.</span></span>

### <a name="other-installation-methods"></a><span data-ttu-id="f35ea-173">Inne metody instalacji</span><span class="sxs-lookup"><span data-stu-id="f35ea-173">Other installation methods</span></span>

<span data-ttu-id="f35ea-174">Aby uzyskać informacje o instalowaniu za pomocą Instalatora platformy sieci Web lub pakietu MSI, zobacz [Inne metody instalacji](other-install.md)</span><span class="sxs-lookup"><span data-stu-id="f35ea-174">For information about installing using the Web Platform Installer or the MSI Package, see [Other installation methods](other-install.md)</span></span>
