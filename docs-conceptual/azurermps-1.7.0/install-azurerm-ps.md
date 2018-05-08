---
title: Instalowanie i konfigurowanie programu Azure PowerShell | Microsoft Docs
description: "Jak zainstalować i skonfigurować program Azure PowerShell do pierwszego użycia."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/17/2017
ms.openlocfilehash: 0c1500a8748a3aa4546c6ce1e8d16a635b056edb
ms.sourcegitcommit: b256bf48e15ee98865de0fae50e7b81878b03a54
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/03/2017
---
# <a name="install-and-configure-azure-powershell"></a><span data-ttu-id="881e9-103">Instalowanie i konfigurowanie programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="881e9-103">Install and configure Azure PowerShell</span></span>

<span data-ttu-id="881e9-104">Instalowanie programu Azure PowerShell z Galerii programu PowerShell jest preferowaną metodą instalacji.</span><span class="sxs-lookup"><span data-stu-id="881e9-104">Installing Azure PowerShell from the PowerShell Gallery is the preferred method of installation.</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="881e9-105">Krok 1. Zainstaluj moduł PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="881e9-105">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="881e9-106">Instalowanie elementów z Galerii programu PowerShell wymaga modułu PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="881e9-106">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="881e9-107">Upewnij się, że masz odpowiednią wersję modułu PowerShellGet oraz spełnione inne wymagania systemowe.</span><span class="sxs-lookup"><span data-stu-id="881e9-107">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="881e9-108">Uruchom następujące polecenie, aby sprawdzić, czy w Twoim systemie został zainstalowany moduł PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="881e9-108">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-Module PowerShellGet -list | Select-Object Name,Version,Path
```

<span data-ttu-id="881e9-109">Powinny zostać wyświetlone dane wyjściowe podobne do poniższych:</span><span class="sxs-lookup"><span data-stu-id="881e9-109">You should see something similar to the following output:</span></span>

```
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="881e9-110">Jeśli nie masz zainstalowanego modułu PowerShellGet, zobacz sekcję [Jak uzyskać moduł PowerShellGet](#how-to-get-powershellget) w niniejszym artykule.</span><span class="sxs-lookup"><span data-stu-id="881e9-110">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget) section of this article.</span></span>

> [!NOTE]
> <span data-ttu-id="881e9-111">Korzystanie z modułu PowerShellGet wymaga zasad wykonania pozwalających uruchamiać skrypty.</span><span class="sxs-lookup"><span data-stu-id="881e9-111">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="881e9-112">Aby uzyskać więcej informacji na temat zasad wykonania programu PowerShell, zobacz [Informacje o zasadach wykonania](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.core/about/about_execution_policies).</span><span class="sxs-lookup"><span data-stu-id="881e9-112">For more information about PowerShell's Execution Policy, see [About Execution Policies](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.core/about/about_execution_policies).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="881e9-113">Krok 2. Zainstaluj program Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="881e9-113">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="881e9-114">Instalacja programu Azure PowerShell z Galerii programu PowerShell wymaga podniesionych uprawnień.</span><span class="sxs-lookup"><span data-stu-id="881e9-114">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="881e9-115">Uruchom następujące polecenie z sesji programu PowerShell z podwyższonym poziomem uprawnień:</span><span class="sxs-lookup"><span data-stu-id="881e9-115">Run the following command from an elevated PowerShell session:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module AzureRM
```

<span data-ttu-id="881e9-116">Galeria programu PowerShell domyślnie nie jest skonfigurowana jako zaufane repozytorium modułu PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="881e9-116">By default, the PowerShell gallery is not configured as a Trusted repository for PowerShellGet.</span></span> <span data-ttu-id="881e9-117">Po pierwszym użyciu Galerii programu PowerShell zostanie wyświetlony następujący komunikat:</span><span class="sxs-lookup"><span data-stu-id="881e9-117">The first time you use the PSGallery you see the following prompt:</span></span>

```
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

<span data-ttu-id="881e9-118">Wybierz odpowiedź „Tak” lub „Tak na wszystkie”, aby kontynuować instalację.</span><span class="sxs-lookup"><span data-stu-id="881e9-118">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="881e9-119">Jeśli masz wersję pakietu NuGet starszą niż 2.8.5.201, zostanie wyświetlony monit o pobranie i zainstalowanie najnowszej wersji pakietu NuGet.</span><span class="sxs-lookup"><span data-stu-id="881e9-119">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="881e9-120">Moduł AzureRM to zbiorczy moduł poleceń cmdlet usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="881e9-120">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="881e9-121">Po zainstalowaniu modułu AzureRM każdy moduł programu Azure PowerShell, który nie został wcześniej zainstalowany, zostanie pobrany i zainstalowany z Galerii programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="881e9-121">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded and from the PowerShell Gallery.</span></span>

<span data-ttu-id="881e9-122">Jeśli masz zainstalowaną poprzednią wersję programu Azure PowerShell, może wystąpić błąd.</span><span class="sxs-lookup"><span data-stu-id="881e9-122">If you have a previous version of Azure PowerShell installed you may receive an error.</span></span> <span data-ttu-id="881e9-123">Aby rozwiązać ten problem, zobacz [Aktualizowanie do nowej wersji programu Azure PowerShell](#update-azps) w dalszej części tego artykułu.</span><span class="sxs-lookup"><span data-stu-id="881e9-123">To resolve this issue, see the [Updating to a new version of Azure PowerShell](#update-azps) section of this article.</span></span>

## <a name="step-3-load-the-azurerm-module"></a><span data-ttu-id="881e9-124">Krok 3. Załaduj moduł AzureRM</span><span class="sxs-lookup"><span data-stu-id="881e9-124">Step 3: Load the AzureRM module</span></span>
<span data-ttu-id="881e9-125">Gdy moduł jest zainstalowany, musisz załadować moduł do swojej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="881e9-125">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="881e9-126">Należy to zrobić w ramach normalnej sesji programu PowerShell (bez podwyższonego poziomu uprawnień).</span><span class="sxs-lookup"><span data-stu-id="881e9-126">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="881e9-127">Moduły są w następujący sposób ładowane przy użyciu polecenia cmdlet `Import-Module`:</span><span class="sxs-lookup"><span data-stu-id="881e9-127">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM
```

## <a name="next-steps"></a><span data-ttu-id="881e9-128">Następne kroki</span><span class="sxs-lookup"><span data-stu-id="881e9-128">Next Steps</span></span>

<span data-ttu-id="881e9-129">Aby uzyskać więcej informacji o korzystaniu z programu Azure PowerShell, zobacz następujące artykuły:</span><span class="sxs-lookup"><span data-stu-id="881e9-129">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="881e9-130">Rozpoczynanie pracy z programem Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="881e9-130">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="frequently-asked-questions"></a><span data-ttu-id="881e9-131">Często zadawane pytania</span><span class="sxs-lookup"><span data-stu-id="881e9-131">Frequently asked questions</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="881e9-132">Jak uzyskać moduł PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="881e9-132">How to get PowerShellGet</span></span>

|<span data-ttu-id="881e9-133">Wersja systemu operacyjnego</span><span class="sxs-lookup"><span data-stu-id="881e9-133">OS Version</span></span>|<span data-ttu-id="881e9-134">Instrukcje dotyczące instalacji</span><span class="sxs-lookup"><span data-stu-id="881e9-134">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="881e9-135">Mam system Windows 10 lub Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="881e9-135">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="881e9-136">Wbudowane w platformę Windows Management Framework (WMF) 5.0 zawartą w systemie operacyjnym</span><span class="sxs-lookup"><span data-stu-id="881e9-136">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="881e9-137">Chcę przeprowadzić uaktualnienie do programu PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="881e9-137">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="881e9-138">Zainstaluj najnowszą wersję platformy WMF</span><span class="sxs-lookup"><span data-stu-id="881e9-138">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|<span data-ttu-id="881e9-139">Używam wersji systemu Windows mającej program PowerShell 3 lub 4</span><span class="sxs-lookup"><span data-stu-id="881e9-139">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|[<span data-ttu-id="881e9-140">Pobierz moduły PackageManagement</span><span class="sxs-lookup"><span data-stu-id="881e9-140">Get the PackageManagement modules</span></span>](http://go.microsoft.com/fwlink/?LinkID=746217)|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a><span data-ttu-id="881e9-141">Sprawdzanie wersji programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="881e9-141">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="881e9-142">Chociaż zachęcamy do jak najszybszego uaktualnienia do najnowszej wersji, różne wersje programu Azure PowerShell są nadal obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="881e9-142">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are support.</span></span> <span data-ttu-id="881e9-143">Aby ustalić zainstalowaną wersję programu Azure PowerShell, uruchom polecenie `Get-Module AzureRM` z wiersza polecenia.</span><span class="sxs-lookup"><span data-stu-id="881e9-143">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -list | Select-Object Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a><span data-ttu-id="881e9-144">Obsługa klasycznych metod wdrażania</span><span class="sxs-lookup"><span data-stu-id="881e9-144">Support for classic deployment methods</span></span>

<span data-ttu-id="881e9-145">Jeśli masz wdrożenia korzystające z klasycznego modelu wdrażania, możesz zainstalować wersję zarządzania usługą programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="881e9-145">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="881e9-146">Aby uzyskać więcej informacji, zobacz [Instalowanie modułu zarządzania usługami programu Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="881e9-146">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="881e9-147">Moduły Azure i AzureRM mają wspólne zależności.</span><span class="sxs-lookup"><span data-stu-id="881e9-147">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="881e9-148">Jeśli korzystasz z modułów Azure i AzureRM, należy zainstalować tę samą wersję każdego pakietu.</span><span class="sxs-lookup"><span data-stu-id="881e9-148">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a id="update-azps"></a><span data-ttu-id="881e9-149">Aktualizowanie do nowej wersji programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="881e9-149">Updating to a new version of Azure PowerShell</span></span>

<span data-ttu-id="881e9-150">Jeśli masz zainstalowaną poprzednią wersję programu Azure PowerShell obejmującą moduł zarządzania usługami, może wystąpić następujący błąd:</span><span class="sxs-lookup"><span data-stu-id="881e9-150">If you have a previous version of Azure PowerShell installed that includes the Service Management module, you may receive the following error:</span></span>

```
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

<span data-ttu-id="881e9-151">Zgodnie z treścią komunikatu o błędzie trzeba zainstalować moduł, podając parametr -AllowClobber.</span><span class="sxs-lookup"><span data-stu-id="881e9-151">As the error message states, you need to use the -AllowClobber parameter to install the module.</span></span> <span data-ttu-id="881e9-152">Użyj następującego polecenia:</span><span class="sxs-lookup"><span data-stu-id="881e9-152">Use the following command:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module AzureRM -AllowClobber
```

<span data-ttu-id="881e9-153">Aby uzyskać więcej informacji, zobacz temat pomocy dotyczący parametru [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span><span class="sxs-lookup"><span data-stu-id="881e9-153">For more information, see the help topic for [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span></span>

### <a name="installing-module-versions-side-by-side"></a><span data-ttu-id="881e9-154">Instalowanie wersji modułu obok siebie</span><span class="sxs-lookup"><span data-stu-id="881e9-154">Installing module versions side by side</span></span>

<span data-ttu-id="881e9-155">Metoda instalacji PowerShellGet jest jedyną metodą, która obsługuje instalowanie wielu wersji.</span><span class="sxs-lookup"><span data-stu-id="881e9-155">The PowerShellGet method of installation is the only method that supports the installation of multiple versions.</span></span> <span data-ttu-id="881e9-156">Na przykład możesz mieć skrypty napisane przy użyciu poprzedniej wersji programu Azure PowerShell, do aktualizacji której nie masz czasu lub zasobów.</span><span class="sxs-lookup"><span data-stu-id="881e9-156">For example, you may have scripts written using a previous version of Azure PowerShell that you don't have the time or resources to updated.</span></span> <span data-ttu-id="881e9-157">Następujące polecenia przedstawiają sposób instalowania wielu wersji programu Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="881e9-157">The following commands illustrate how to install multiple versions of Azure PowerShell:</span></span>

```powershell
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="881e9-158">Tylko jedna wersja modułu może zostać załadowana w sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="881e9-158">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="881e9-159">Musisz otworzyć nowe okno programu PowerShell i użyć polecenia `Import-Module`, aby zaimportować określoną wersję poleceń cmdlet modułu AzureRM:</span><span class="sxs-lookup"><span data-stu-id="881e9-159">You must open a new PowerShell window and use `Import-Module` to import a specific version of the AzureRM cmdlets:</span></span>

```powershell
Import-Module AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> <span data-ttu-id="881e9-160">Wersja 2.1.0 i wersja 1.2.6 to pierwsze wersje modułu przeznaczone do instalacji i używania obok siebie.</span><span class="sxs-lookup"><span data-stu-id="881e9-160">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="881e9-161">Załadowanie starszej wersji programu Azure PowerShell powoduje załadowanie niezgodnych wersji modułu **AzureRM.Profile**.</span><span class="sxs-lookup"><span data-stu-id="881e9-161">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="881e9-162">W wyniku tego każde wykonanie polecenia cmdlet powoduje wyświetlenie polecenia cmdlet z monitem o zalogowanie się.</span><span class="sxs-lookup"><span data-stu-id="881e9-162">This results in the cmdlets prompting you to log in whenever you execute a cmdlet.</span></span>

### <a name="other-installation-methods"></a><span data-ttu-id="881e9-163">Inne metody instalacji</span><span class="sxs-lookup"><span data-stu-id="881e9-163">Other installation methods</span></span>

<span data-ttu-id="881e9-164">Aby uzyskać informacje o instalowaniu za pomocą Instalatora platformy sieci Web lub pakietu MSI, zobacz [Inne metody instalacji](other-install.md)</span><span class="sxs-lookup"><span data-stu-id="881e9-164">For information about installing using the Web Platform Installer or the MSI Package, see [Other installation methods](other-install.md)</span></span>
