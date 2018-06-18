---
title: Instalowanie programu Azure PowerShell za pomocą modułu PowerShellGet
description: Jak zainstalować program Azure PowerShell za pomocą modułu PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/31/2018
ms.openlocfilehash: 9b7046157e32a5c8473210e9840f9ae1b2f45902
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323105"
---
# <a name="install-azure-powershell-with-powershellget"></a><span data-ttu-id="9bf36-103">Instalowanie programu Azure PowerShell za pomocą modułu PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="9bf36-103">Install Azure PowerShell with PowerShellGet</span></span>

<span data-ttu-id="9bf36-104">W tym artykule opisano kroki instalowania modułów programu Azure PowerShell w środowisku systemu Windows przy użyciu modułu PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="9bf36-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment using PowerShellGet.</span></span>  <span data-ttu-id="9bf36-105">Jest to preferowany sposób instalacji programu Azure PowerShell, ale jeśli wolisz go zainstalować za pomocą Instalatora platformy internetowej lub pakietu MSI, zobacz [Inne metody instalacji](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="9bf36-105">This is the preferred way to install Azure PowerShell, but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="9bf36-106">Jeśli chcesz korzystać z programu Azure PowerShell w systemie macOS lub Linux, zobacz następujący artykuł: [Instalowanie i konfigurowanie programu Azure PowerShell w systemach macOS i Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="9bf36-106">If you want to use Azure PowerShell on macOS or Linux, see the following article: [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="system-requirements"></a><span data-ttu-id="9bf36-107">Wymagania systemowe</span><span class="sxs-lookup"><span data-stu-id="9bf36-107">System requirements</span></span>

<span data-ttu-id="9bf36-108">Usługa Azure PowerShell w wersji 6.1.0 wymaga programu PowerShell w wersji 5.0 lub nowszej.</span><span class="sxs-lookup"><span data-stu-id="9bf36-108">Azure PowerShell version 6.1.0 requires version 5.0 (or higher) of PowerShell.</span></span> <span data-ttu-id="9bf36-109">Aby uzyskać informacje dotyczące uaktualnienia programu PowerShell do wersji 5.0, zobacz [Upgrading existing Windows PowerShell (Uaktualnianie istniejącego programu Windows PowerShell)](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="9bf36-109">For information on upgrading to PowerShell 5.0, see [Upgrading existing Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

<span data-ttu-id="9bf36-110">Moduł PowerShellGet jest automatycznie uwzględniony jako część programu PowerShell 5.0.</span><span class="sxs-lookup"><span data-stu-id="9bf36-110">PowerShellGet is automatically included as part of PowerShell 5.0.</span></span>

## <a name="install-or-update-the-azure-powershell-module"></a><span data-ttu-id="9bf36-111">Instalowanie lub aktualizowanie modułu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="9bf36-111">Install or update the Azure PowerShell module</span></span>

<span data-ttu-id="9bf36-112">Instalacja programu Azure PowerShell z Galerii programu PowerShell wymaga podniesionych uprawnień.</span><span class="sxs-lookup"><span data-stu-id="9bf36-112">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="9bf36-113">Uruchom następujące polecenie z sesji programu PowerShell z podwyższonym poziomem uprawnień:</span><span class="sxs-lookup"><span data-stu-id="9bf36-113">Run the following command from an elevated PowerShell session:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

> [!IMPORTANT]
> <span data-ttu-id="9bf36-114">To polecenie zaktualizuje dowolną istniejącą instalację programu Azure PowerShell w Twoim systemie.</span><span class="sxs-lookup"><span data-stu-id="9bf36-114">This command will update any existing installation of Azure PowerShell on your system.</span></span> <span data-ttu-id="9bf36-115">Jeśli potrzebujesz mieć zainstalowaną więcej niż jedną wersję, zobacz odpowiedź na pytanie [Czy mogę zainstalować wiele wersji programu Azure PowerShell?](#multiple-versions) w sekcji Często zadawane pytania</span><span class="sxs-lookup"><span data-stu-id="9bf36-115">If you need to have more than one version installed, see the FAQ answer for [Can I install multiple versions of Azure PowerShell?](#multiple-versions)</span></span>

<span data-ttu-id="9bf36-116">Galeria programu PowerShell domyślnie nie jest skonfigurowana jako zaufane repozytorium modułu PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="9bf36-116">By default, the PowerShell gallery is not configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="9bf36-117">Po pierwszym użyciu Galerii programu PowerShell zostanie wyświetlony następujący komunikat:</span><span class="sxs-lookup"><span data-stu-id="9bf36-117">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="9bf36-118">Wybierz odpowiedź „Tak” lub „Tak na wszystkie”, aby kontynuować instalację.</span><span class="sxs-lookup"><span data-stu-id="9bf36-118">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="9bf36-119">Jeśli masz wersję pakietu NuGet starszą niż 2.8.5.201, zostanie wyświetlony monit o pobranie i zainstalowanie najnowszej wersji pakietu NuGet.</span><span class="sxs-lookup"><span data-stu-id="9bf36-119">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="9bf36-120">Moduł AzureRM to zbiorczy moduł poleceń cmdlet usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="9bf36-120">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="9bf36-121">Po zainstalowaniu modułu AzureRM każdy moduł programu Azure PowerShell, który nie został wcześniej zainstalowany, zostanie pobrany z Galerii programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9bf36-121">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded from the PowerShell Gallery.</span></span>

## <a name="load-the-azure-powershell-module"></a><span data-ttu-id="9bf36-122">Ładowanie modułu programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="9bf36-122">Load the Azure PowerShell module</span></span>

<span data-ttu-id="9bf36-123">Gdy moduł jest zainstalowany, musisz załadować moduł do swojej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9bf36-123">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="9bf36-124">Należy to zrobić w ramach normalnej sesji programu PowerShell (bez podwyższonego poziomu uprawnień).</span><span class="sxs-lookup"><span data-stu-id="9bf36-124">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="9bf36-125">Moduły są w następujący sposób ładowane przy użyciu polecenia cmdlet `Import-Module`:</span><span class="sxs-lookup"><span data-stu-id="9bf36-125">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module -Name AzureRM
```

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="9bf36-126">Zgłaszanie problemów i przesyłanie opinii</span><span class="sxs-lookup"><span data-stu-id="9bf36-126">Reporting issues and feedback</span></span>

<span data-ttu-id="9bf36-127">Jeśli napotkasz jakiekolwiek usterki w narzędziu, [prześlij zgłoszenie w witrynie GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="9bf36-127">If you encounter any bugs with the tool, please [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="9bf36-128">Aby przekazać opinię z wiersza polecenia, użyj polecenia cmdlet `Send-Feedback`.</span><span class="sxs-lookup"><span data-stu-id="9bf36-128">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="9bf36-129">Następne kroki</span><span class="sxs-lookup"><span data-stu-id="9bf36-129">Next Steps</span></span>

<span data-ttu-id="9bf36-130">Aby uzyskać więcej informacji o korzystaniu z programu Azure PowerShell, zobacz następujące artykuły:</span><span class="sxs-lookup"><span data-stu-id="9bf36-130">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="9bf36-131">Rozpoczynanie pracy z programem Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="9bf36-131">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="frequently-asked-questions"></a><span data-ttu-id="9bf36-132">Często zadawane pytania</span><span class="sxs-lookup"><span data-stu-id="9bf36-132">Frequently asked questions</span></span>

### <a id="helpmechoose"></a><span data-ttu-id="9bf36-133">Jak mogę sprawdzić wersję programu Azure PowerShell?</span><span class="sxs-lookup"><span data-stu-id="9bf36-133">How do I check the version of Azure PowerShell?</span></span>

<span data-ttu-id="9bf36-134">Chociaż zachęcamy do jak najszybszego uaktualnienia do najnowszej wersji, różne wersje programu Azure PowerShell są nadal obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="9bf36-134">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="9bf36-135">Aby ustalić zainstalowaną wersję programu Azure PowerShell, uruchom polecenie `Get-Module AzureRM` z wiersza polecenia.</span><span class="sxs-lookup"><span data-stu-id="9bf36-135">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="can-i-use-azure-powershell-for-azure-classic-deployments"></a><span data-ttu-id="9bf36-136">Czy mogę użyć programu Azure PowerShell na potrzeby klasycznych wdrożeń platformy Azure?</span><span class="sxs-lookup"><span data-stu-id="9bf36-136">Can I use Azure PowerShell for Azure Classic deployments?</span></span>

<span data-ttu-id="9bf36-137">Jeśli masz wdrożenia korzystające z klasycznego modelu wdrażania, możesz zainstalować wersję zarządzania usługą programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9bf36-137">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="9bf36-138">Aby uzyskać więcej informacji, zobacz [Instalowanie modułu Azure PowerShell Service Management](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="9bf36-138">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="9bf36-139">Moduły Azure i AzureRM mają wspólne zależności.</span><span class="sxs-lookup"><span data-stu-id="9bf36-139">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="9bf36-140">Jeśli korzystasz z modułów Azure i AzureRM, należy zainstalować tę samą wersję każdego pakietu.</span><span class="sxs-lookup"><span data-stu-id="9bf36-140">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a name="a-namemultiple-versionscan-i-install-multiple-versions-of-azure-powershell"></a><span data-ttu-id="9bf36-141"><a name="multiple-versions"/>Czy mogę zainstalować wiele wersji programu Azure PowerShell?</span><span class="sxs-lookup"><span data-stu-id="9bf36-141"><a name="multiple-versions"/>Can I install multiple versions of Azure PowerShell?</span></span>

<span data-ttu-id="9bf36-142">Moduł PowerShellGet to jedyna metoda instalacji, która obsługuje wiele wersji.</span><span class="sxs-lookup"><span data-stu-id="9bf36-142">PowerShellGet the only method of installation that supports multiple versions.</span></span> <span data-ttu-id="9bf36-143">Aby zainstalować wiele wersji, możesz dodać parametr `-RequiredVersion` do polecenia cmdlet `Install-Module`.</span><span class="sxs-lookup"><span data-stu-id="9bf36-143">To install multiple versions, you can add the `-RequiredVersion` parameter to the `Install-Module` cmdlet.</span></span> <span data-ttu-id="9bf36-144">Na przykład w celu zainstalowania wersji 6.1.0 oraz 1.2.9:</span><span class="sxs-lookup"><span data-stu-id="9bf36-144">For example, to install both versions 6.1.0 and 1.2.9:</span></span>

```powershell
Install-Module -Name AzureRM -RequiredVersion 6.1.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="9bf36-145">Tylko jedna wersja modułu może zostać załadowana w sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9bf36-145">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="9bf36-146">Musisz otworzyć nowe okno programu PowerShell i użyć polecenia `Import-Module`, aby zaimportować określoną wersję modułu programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9bf36-146">You must open a new PowerShell window and use `Import-Module` to import a specific version of the Azure PowerShell module.</span></span>

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> <span data-ttu-id="9bf36-147">Wersja 2.1.0 i wersja 1.2.6 to pierwsze wersje modułu przeznaczone do instalacji i używania obok siebie.</span><span class="sxs-lookup"><span data-stu-id="9bf36-147">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="9bf36-148">Załadowanie starszej wersji programu Azure PowerShell powoduje załadowanie niezgodnych wersji modułu **AzureRM.Profile**.</span><span class="sxs-lookup"><span data-stu-id="9bf36-148">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="9bf36-149">W wyniku tego każde wykonanie polecenia cmdlet powoduje wyświetlenie polecenia cmdlet z monitem o zalogowanie się.</span><span class="sxs-lookup"><span data-stu-id="9bf36-149">This results in the cmdlets prompting you to log in whenever you execute a cmdlet.</span></span>
