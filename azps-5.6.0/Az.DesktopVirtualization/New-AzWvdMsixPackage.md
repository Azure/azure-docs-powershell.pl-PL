---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/new-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
ms.openlocfilehash: ecb5b1200bacab12f7715600b7fcf60b78b81092
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966145"
---
# <span data-ttu-id="83019-101">New-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="83019-101">New-AzWvdMsixPackage</span></span>

## <span data-ttu-id="83019-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83019-102">SYNOPSIS</span></span>
<span data-ttu-id="83019-103">Utwórz lub zaktualizuj pakiet MSIX.</span><span class="sxs-lookup"><span data-stu-id="83019-103">Create or update a MSIX package.</span></span>

## <span data-ttu-id="83019-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="83019-104">SYNTAX</span></span>

### <span data-ttu-id="83019-105">CreateExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="83019-105">CreateExpanded (Default)</span></span>
```
New-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-LastUpdated <DateTime>] [-PackageApplication <IMsixPackageApplications[]>]
 [-PackageDependency <IMsixPackageDependencies[]>] [-PackageFamilyName <String>] [-PackageName <String>]
 [-PackageRelativePath <String>] [-Version <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="83019-106">PackageAlias</span><span class="sxs-lookup"><span data-stu-id="83019-106">PackageAlias</span></span>
```
New-AzWvdMsixPackage -HostPoolName <String> -PackageAlias <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="83019-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="83019-107">DESCRIPTION</span></span>
<span data-ttu-id="83019-108">Utwórz lub zaktualizuj pakiet MSIX.</span><span class="sxs-lookup"><span data-stu-id="83019-108">Create or update a MSIX package.</span></span>

## <span data-ttu-id="83019-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="83019-109">EXAMPLES</span></span>

### <span data-ttu-id="83019-110">Przykład 1. Tworzy nowy pakiet MSIX w buforze hosta za pomocą aliasu pakietu</span><span class="sxs-lookup"><span data-stu-id="83019-110">Example 1: Creates New MSIX Package in the HostPool via Package Alias</span></span>
```powershell
PS C:\> New-AzWvdMsixPackage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
      -PackageAlias packagealias `
      -ImagePath ImagePathURI  `
```

<span data-ttu-id="83019-111">To polecenie dodaje pakiet MSIX z określonej ścieżki obrazu do usługi HostPool</span><span class="sxs-lookup"><span data-stu-id="83019-111">This command adds MSIX package from specified image path to HostPool</span></span>

### <span data-ttu-id="83019-112">Przykład 2. Tworzy nowy pakiet MSIX w buforze hosta</span><span class="sxs-lookup"><span data-stu-id="83019-112">Example 2: Creates New MSIX Package in the HostPool</span></span>
```powershell
PS C:\> New-AzWvdMsixPackage -FullName PackageFullName `
                            -HostPoolName HostPoolName `
                            -ResourceGroupName ResourceGroupName ` 
                            -SubscriptionId SubscriptionId ` 
                            -DisplayName displayname `
                            -ImagePath imageURI ` 
                            -IsActive:$false `
                            -IsRegularRegistration:$false `
                            -LastUpdated datelastupdated `
                            -PackageApplication $apps `
                            -PackageDependency $deps `
                            -PackageFamilyName packagefamilyname `
                            -PackageName packagename `
                            -PackageRelativePath packagerelativepath `
                            -Version packageversion `

Name                              Type
----                              ----
HotPoolName/PackageFullName      Microsoft.DesktopVirtualization/hostpools/msixpackages

```

<span data-ttu-id="83019-113">To polecenie dodaje pakiet MSIX w określonym buforze hosta</span><span class="sxs-lookup"><span data-stu-id="83019-113">This command adds MSIX Package in the specified HostPool</span></span>

## <span data-ttu-id="83019-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83019-114">PARAMETERS</span></span>

### <span data-ttu-id="83019-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83019-115">-DefaultProfile</span></span>
<span data-ttu-id="83019-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="83019-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83019-117">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="83019-117">-DisplayName</span></span>
<span data-ttu-id="83019-118">Przyjazna dla użytkownika nazwa wyświetlana w portalu.</span><span class="sxs-lookup"><span data-stu-id="83019-118">User friendly Name to be displayed in the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83019-119">-FullName</span><span class="sxs-lookup"><span data-stu-id="83019-119">-FullName</span></span>
<span data-ttu-id="83019-120">Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="83019-120">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83019-121">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="83019-121">-HostPoolName</span></span>
<span data-ttu-id="83019-122">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="83019-122">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83019-123">— ImagePath</span><span class="sxs-lookup"><span data-stu-id="83019-123">-ImagePath</span></span>
<span data-ttu-id="83019-124">Ścieżka obrazu VHD/CIM w dziele sieciowym.</span><span class="sxs-lookup"><span data-stu-id="83019-124">VHD/CIM image path on Network Share.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83019-125">—IsActive</span><span class="sxs-lookup"><span data-stu-id="83019-125">-IsActive</span></span>
<span data-ttu-id="83019-126">Upewnij się, że ta wersja pakietu jest aktywna w całej buforze hosta.</span><span class="sxs-lookup"><span data-stu-id="83019-126">Make this version of the package the active one across the hostpool.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83019-127">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="83019-127">-IsRegularRegistration</span></span>
<span data-ttu-id="83019-128">Określa sposób rejestrowania pakietu w kanale informacyjnym.</span><span class="sxs-lookup"><span data-stu-id="83019-128">Specifies how to register Package in feed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83019-129">-LastUpdated</span><span class="sxs-lookup"><span data-stu-id="83019-129">-LastUpdated</span></span>
<span data-ttu-id="83019-130">Data ostatniej aktualizacji pakietu, która została znaleziona w appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="83019-130">Date Package was last updated, found in the appxmanifest.xml.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83019-131">-PackageAlias</span><span class="sxs-lookup"><span data-stu-id="83019-131">-PackageAlias</span></span>
<span data-ttu-id="83019-132">Alias pakietu z wyodrębnienia obrazu MSIX</span><span class="sxs-lookup"><span data-stu-id="83019-132">Package Alias from extract MSIX Image</span></span>

```yaml
Type: System.String
Parameter Sets: PackageAlias
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83019-133">-PackageApplication</span><span class="sxs-lookup"><span data-stu-id="83019-133">-PackageApplication</span></span>
<span data-ttu-id="83019-134">Lista aplikacji pakietu.</span><span class="sxs-lookup"><span data-stu-id="83019-134">List of package applications.</span></span>

<span data-ttu-id="83019-135">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach PACKAGEAPPLICATION i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="83019-135">To construct, see NOTES section for PACKAGEAPPLICATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackageApplications[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83019-136">-PackageDependency</span><span class="sxs-lookup"><span data-stu-id="83019-136">-PackageDependency</span></span>
<span data-ttu-id="83019-137">Lista zależności pakietów.</span><span class="sxs-lookup"><span data-stu-id="83019-137">List of package dependencies.</span></span>

<span data-ttu-id="83019-138">Aby skonstruować, zobacz sekcję NOTES, aby uzyskać informacje o właściwościach PACKAGEDEPENDENCY i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="83019-138">To construct, see NOTES section for PACKAGEDEPENDENCY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackageDependencies[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83019-139">-PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="83019-139">-PackageFamilyName</span></span>
<span data-ttu-id="83019-140">Spakuj nazwę rodziny z appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="83019-140">Package Family Name from appxmanifest.xml.</span></span>
<span data-ttu-id="83019-141">Zawiera nazwę pakietu i nazwę wydawcy.</span><span class="sxs-lookup"><span data-stu-id="83019-141">Contains Package Name and Publisher name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83019-142">-PackageName</span><span class="sxs-lookup"><span data-stu-id="83019-142">-PackageName</span></span>
<span data-ttu-id="83019-143">Nazwa pakietu z appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="83019-143">Package Name from appxmanifest.xml.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83019-144">-PackageRelativePath</span><span class="sxs-lookup"><span data-stu-id="83019-144">-PackageRelativePath</span></span>
<span data-ttu-id="83019-145">Ścieżka względna do pakietu wewnątrz obrazu.</span><span class="sxs-lookup"><span data-stu-id="83019-145">Relative Path to the package inside the image.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83019-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83019-146">-ResourceGroupName</span></span>
<span data-ttu-id="83019-147">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="83019-147">The name of the resource group.</span></span>
<span data-ttu-id="83019-148">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="83019-148">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83019-149">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="83019-149">-SubscriptionId</span></span>
<span data-ttu-id="83019-150">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="83019-150">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83019-151">— Wersja</span><span class="sxs-lookup"><span data-stu-id="83019-151">-Version</span></span>
<span data-ttu-id="83019-152">Wersja pakietu znaleziona w appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="83019-152">Package Version found in the appxmanifest.xml.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83019-153">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="83019-153">-Confirm</span></span>
<span data-ttu-id="83019-154">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="83019-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83019-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83019-155">-WhatIf</span></span>
<span data-ttu-id="83019-156">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83019-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83019-157">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="83019-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83019-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83019-158">CommonParameters</span></span>
<span data-ttu-id="83019-159">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83019-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83019-160">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83019-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83019-161">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83019-161">INPUTS</span></span>

## <span data-ttu-id="83019-162">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83019-162">OUTPUTS</span></span>

### <span data-ttu-id="83019-163">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="83019-163">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="83019-164">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="83019-164">NOTES</span></span>

<span data-ttu-id="83019-165">ALIASY</span><span class="sxs-lookup"><span data-stu-id="83019-165">ALIASES</span></span>

<span data-ttu-id="83019-166">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="83019-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="83019-167">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="83019-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="83019-168">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="83019-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="83019-169">PACKAGEAPPLICATION <IMsixPackageApplications[]>: Lista aplikacji pakietu.</span><span class="sxs-lookup"><span data-stu-id="83019-169">PACKAGEAPPLICATION <IMsixPackageApplications[]>: List of package applications.</span></span> 
  - <span data-ttu-id="83019-170">`[AppId <String>]`: Identyfikator aplikacji pakietu, który został znaleziony w appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="83019-170">`[AppId <String>]`: Package Application Id, found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="83019-171">`[AppUserModelId <String>]`: Służy do aktywowania aplikacji pakietu.</span><span class="sxs-lookup"><span data-stu-id="83019-171">`[AppUserModelId <String>]`: Used to activate Package Application.</span></span> <span data-ttu-id="83019-172">Składa się z nazwy pakietu i pola ApplicationID.</span><span class="sxs-lookup"><span data-stu-id="83019-172">Consists of Package Name and ApplicationID.</span></span> <span data-ttu-id="83019-173">Znaleziono w appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="83019-173">Found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="83019-174">`[Description <String>]`: Opis aplikacji pakietu.</span><span class="sxs-lookup"><span data-stu-id="83019-174">`[Description <String>]`: Description of Package Application.</span></span>
  - <span data-ttu-id="83019-175">`[FriendlyName <String>]`: przyjazna dla użytkownika nazwa.</span><span class="sxs-lookup"><span data-stu-id="83019-175">`[FriendlyName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="83019-176">`[IconImageName <String>]`: przyjazna dla użytkownika nazwa.</span><span class="sxs-lookup"><span data-stu-id="83019-176">`[IconImageName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="83019-177">`[RawIcon <Byte[]>]`: ikona ciągu 64-bitowego jako tablica bajtowa.</span><span class="sxs-lookup"><span data-stu-id="83019-177">`[RawIcon <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>
  - <span data-ttu-id="83019-178">`[RawPng <Byte[]>]`: ikona ciągu 64-bitowego jako tablica bajtowa.</span><span class="sxs-lookup"><span data-stu-id="83019-178">`[RawPng <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>

<span data-ttu-id="83019-179">PACKAGEDEPENDENCY <IMsixPackageDependencies[]>: Lista zależności pakietów.</span><span class="sxs-lookup"><span data-stu-id="83019-179">PACKAGEDEPENDENCY <IMsixPackageDependencies[]>: List of package dependencies.</span></span> 
  - <span data-ttu-id="83019-180">`[DependencyName <String>]`: Nazwa zależności pakietu.</span><span class="sxs-lookup"><span data-stu-id="83019-180">`[DependencyName <String>]`: Name of package dependency.</span></span>
  - <span data-ttu-id="83019-181">`[MinVersion <String>]`: Wymagana wersja zależności.</span><span class="sxs-lookup"><span data-stu-id="83019-181">`[MinVersion <String>]`: Dependency version required.</span></span>
  - <span data-ttu-id="83019-182">`[Publisher <String>]`: nazwa wydawcy zależności.</span><span class="sxs-lookup"><span data-stu-id="83019-182">`[Publisher <String>]`: Name of dependency publisher.</span></span>

## <span data-ttu-id="83019-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83019-183">RELATED LINKS</span></span>

