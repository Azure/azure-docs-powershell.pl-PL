---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
ms.openlocfilehash: fd5dd920863d4bd53257cfe2170e83f53c620096
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357618"
---
# <span data-ttu-id="e3262-101">New-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="e3262-101">New-AzWvdMsixPackage</span></span>

## <span data-ttu-id="e3262-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e3262-102">SYNOPSIS</span></span>
<span data-ttu-id="e3262-103">Utwórz lub zaktualizuj pakiet MSIX.</span><span class="sxs-lookup"><span data-stu-id="e3262-103">Create or update a MSIX package.</span></span>

## <span data-ttu-id="e3262-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e3262-104">SYNTAX</span></span>

### <span data-ttu-id="e3262-105">Rozszerzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e3262-105">CreateExpanded (Default)</span></span>
```
New-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-LastUpdated <DateTime>] [-PackageApplication <IMsixPackageApplications[]>]
 [-PackageDependency <IMsixPackageDependencies[]>] [-PackageFamilyName <String>] [-PackageName <String>]
 [-PackageRelativePath <String>] [-Version <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e3262-106">PackageAlias</span><span class="sxs-lookup"><span data-stu-id="e3262-106">PackageAlias</span></span>
```
New-AzWvdMsixPackage -HostPoolName <String> -PackageAlias <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e3262-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e3262-107">DESCRIPTION</span></span>
<span data-ttu-id="e3262-108">Utwórz lub zaktualizuj pakiet MSIX.</span><span class="sxs-lookup"><span data-stu-id="e3262-108">Create or update a MSIX package.</span></span>

## <span data-ttu-id="e3262-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e3262-109">EXAMPLES</span></span>

### <span data-ttu-id="e3262-110">Przykład 1: tworzy nowy pakiet MSIX w HostPool za pośrednictwem aliasu pakietu</span><span class="sxs-lookup"><span data-stu-id="e3262-110">Example 1: Creates New MSIX Package in the HostPool via Package Alias</span></span>
```powershell
PS C:\> New-AzWvdMsixPackage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
      -PackageAlias packagealias `
      -ImagePath ImagePathURI  `
```

<span data-ttu-id="e3262-111">To polecenie dodaje pakiet MSIX z określonej ścieżki obrazu do HostPool</span><span class="sxs-lookup"><span data-stu-id="e3262-111">This command adds MSIX package from specified image path to HostPool</span></span>

### <span data-ttu-id="e3262-112">Przykład 2: tworzy nowy pakiet MSIX w HostPool</span><span class="sxs-lookup"><span data-stu-id="e3262-112">Example 2: Creates New MSIX Package in the HostPool</span></span>
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

<span data-ttu-id="e3262-113">To polecenie dodaje pakiet MSIX w określonym HostPool</span><span class="sxs-lookup"><span data-stu-id="e3262-113">This command adds MSIX Package in the specified HostPool</span></span>

## <span data-ttu-id="e3262-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e3262-114">PARAMETERS</span></span>

### <span data-ttu-id="e3262-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3262-115">-DefaultProfile</span></span>
<span data-ttu-id="e3262-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e3262-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3262-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e3262-117">-DisplayName</span></span>
<span data-ttu-id="e3262-118">Przyjazna nazwa użytkownika, która ma być wyświetlana w portalu.</span><span class="sxs-lookup"><span data-stu-id="e3262-118">User friendly Name to be displayed in the portal.</span></span>

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

### <span data-ttu-id="e3262-119">-ImięNazwisko</span><span class="sxs-lookup"><span data-stu-id="e3262-119">-FullName</span></span>
<span data-ttu-id="e3262-120">Pakiet specyficzny dla wersji pełna nazwa pakietu MSIX w określonym hostpool</span><span class="sxs-lookup"><span data-stu-id="e3262-120">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="e3262-121">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="e3262-121">-HostPoolName</span></span>
<span data-ttu-id="e3262-122">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="e3262-122">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="e3262-123">-ImagePath</span><span class="sxs-lookup"><span data-stu-id="e3262-123">-ImagePath</span></span>
<span data-ttu-id="e3262-124">Ścieżka obrazu VHD/wirtualnego dysku twardego w udziale sieciowym.</span><span class="sxs-lookup"><span data-stu-id="e3262-124">VHD/CIM image path on Network Share.</span></span>

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

### <span data-ttu-id="e3262-125">-IsActive</span><span class="sxs-lookup"><span data-stu-id="e3262-125">-IsActive</span></span>
<span data-ttu-id="e3262-126">Udostępnij tę wersję pakietu jako aktywną w hostpool.</span><span class="sxs-lookup"><span data-stu-id="e3262-126">Make this version of the package the active one across the hostpool.</span></span>

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

### <span data-ttu-id="e3262-127">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="e3262-127">-IsRegularRegistration</span></span>
<span data-ttu-id="e3262-128">Określa sposób rejestrowania pakietu w kanale informacyjnym.</span><span class="sxs-lookup"><span data-stu-id="e3262-128">Specifies how to register Package in feed.</span></span>

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

### <span data-ttu-id="e3262-129">-LastUpdated</span><span class="sxs-lookup"><span data-stu-id="e3262-129">-LastUpdated</span></span>
<span data-ttu-id="e3262-130">Data ostatniej aktualizacji pakietu, znaleziono w appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="e3262-130">Date Package was last updated, found in the appxmanifest.xml.</span></span>

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

### <span data-ttu-id="e3262-131">-PackageAlias</span><span class="sxs-lookup"><span data-stu-id="e3262-131">-PackageAlias</span></span>
<span data-ttu-id="e3262-132">Alias pakietu z wyodrębnienia obrazu MSIX</span><span class="sxs-lookup"><span data-stu-id="e3262-132">Package Alias from extract MSIX Image</span></span>

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

### <span data-ttu-id="e3262-133">-PackageApplication</span><span class="sxs-lookup"><span data-stu-id="e3262-133">-PackageApplication</span></span>
<span data-ttu-id="e3262-134">Lista aplikacji pakietu.</span><span class="sxs-lookup"><span data-stu-id="e3262-134">List of package applications.</span></span>

<span data-ttu-id="e3262-135">Aby skonstruować, zobacz sekcję notatki dla właściwości PACKAGEAPPLICATION i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="e3262-135">To construct, see NOTES section for PACKAGEAPPLICATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackageApplications[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3262-136">-PackageDependency</span><span class="sxs-lookup"><span data-stu-id="e3262-136">-PackageDependency</span></span>
<span data-ttu-id="e3262-137">Lista zależności pakietu.</span><span class="sxs-lookup"><span data-stu-id="e3262-137">List of package dependencies.</span></span>

<span data-ttu-id="e3262-138">Aby skonstruować, zobacz sekcję notatki dla właściwości PACKAGEDEPENDENCY i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="e3262-138">To construct, see NOTES section for PACKAGEDEPENDENCY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackageDependencies[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3262-139">-PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="e3262-139">-PackageFamilyName</span></span>
<span data-ttu-id="e3262-140">Nazwa rodziny pakietów od appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="e3262-140">Package Family Name from appxmanifest.xml.</span></span>
<span data-ttu-id="e3262-141">Zawiera nazwę pakietu i nazwę wydawcy.</span><span class="sxs-lookup"><span data-stu-id="e3262-141">Contains Package Name and Publisher name.</span></span>

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

### <span data-ttu-id="e3262-142">-PackageName</span><span class="sxs-lookup"><span data-stu-id="e3262-142">-PackageName</span></span>
<span data-ttu-id="e3262-143">Nazwa pakietu z appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="e3262-143">Package Name from appxmanifest.xml.</span></span>

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

### <span data-ttu-id="e3262-144">-PackageRelativePath</span><span class="sxs-lookup"><span data-stu-id="e3262-144">-PackageRelativePath</span></span>
<span data-ttu-id="e3262-145">Względna ścieżka do pakietu w obrazie.</span><span class="sxs-lookup"><span data-stu-id="e3262-145">Relative Path to the package inside the image.</span></span>

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

### <span data-ttu-id="e3262-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3262-146">-ResourceGroupName</span></span>
<span data-ttu-id="e3262-147">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e3262-147">The name of the resource group.</span></span>
<span data-ttu-id="e3262-148">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="e3262-148">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e3262-149">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e3262-149">-SubscriptionId</span></span>
<span data-ttu-id="e3262-150">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="e3262-150">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e3262-151">-Version</span><span class="sxs-lookup"><span data-stu-id="e3262-151">-Version</span></span>
<span data-ttu-id="e3262-152">Wersja pakietu znaleziona w appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="e3262-152">Package Version found in the appxmanifest.xml.</span></span>

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

### <span data-ttu-id="e3262-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e3262-153">-Confirm</span></span>
<span data-ttu-id="e3262-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3262-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3262-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3262-155">-WhatIf</span></span>
<span data-ttu-id="e3262-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3262-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3262-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e3262-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3262-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3262-158">CommonParameters</span></span>
<span data-ttu-id="e3262-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3262-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3262-160">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3262-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3262-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3262-161">INPUTS</span></span>

## <span data-ttu-id="e3262-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e3262-162">OUTPUTS</span></span>

### <span data-ttu-id="e3262-163">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20201019Preview. IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="e3262-163">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackage</span></span>

## <span data-ttu-id="e3262-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e3262-164">NOTES</span></span>

<span data-ttu-id="e3262-165">PISUJE</span><span class="sxs-lookup"><span data-stu-id="e3262-165">ALIASES</span></span>

<span data-ttu-id="e3262-166">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e3262-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e3262-167">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="e3262-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e3262-168">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e3262-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e3262-169">PACKAGEAPPLICATION <IMsixPackageApplications [] >: Lista aplikacji pakietu.</span><span class="sxs-lookup"><span data-stu-id="e3262-169">PACKAGEAPPLICATION <IMsixPackageApplications[]>: List of package applications.</span></span> 
  - <span data-ttu-id="e3262-170">`[AppId <String>]`: Identyfikator aplikacji pakietu odnaleziony w appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="e3262-170">`[AppId <String>]`: Package Application Id, found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="e3262-171">`[AppUserModelId <String>]`: Służy do aktywowania aplikacji pakietu.</span><span class="sxs-lookup"><span data-stu-id="e3262-171">`[AppUserModelId <String>]`: Used to activate Package Application.</span></span> <span data-ttu-id="e3262-172">Składa się z nazwy pakietu i aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e3262-172">Consists of Package Name and ApplicationID.</span></span> <span data-ttu-id="e3262-173">Dostępne w appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="e3262-173">Found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="e3262-174">`[Description <String>]`: Opis aplikacji pakietu.</span><span class="sxs-lookup"><span data-stu-id="e3262-174">`[Description <String>]`: Description of Package Application.</span></span>
  - <span data-ttu-id="e3262-175">`[FriendlyName <String>]`: Przyjazna nazwa użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e3262-175">`[FriendlyName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="e3262-176">`[IconImageName <String>]`: Przyjazna nazwa użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e3262-176">`[IconImageName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="e3262-177">`[RawIcon <Byte[]>]`: ikona 64a ciąg bitowy jako tablica bajtów.</span><span class="sxs-lookup"><span data-stu-id="e3262-177">`[RawIcon <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>
  - <span data-ttu-id="e3262-178">`[RawPng <Byte[]>]`: ikona 64a ciąg bitowy jako tablica bajtów.</span><span class="sxs-lookup"><span data-stu-id="e3262-178">`[RawPng <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>

<span data-ttu-id="e3262-179">PACKAGEDEPENDENCY <IMsixPackageDependencies [] >: Lista zależności pakietu.</span><span class="sxs-lookup"><span data-stu-id="e3262-179">PACKAGEDEPENDENCY <IMsixPackageDependencies[]>: List of package dependencies.</span></span> 
  - <span data-ttu-id="e3262-180">`[DependencyName <String>]`: Nazwa zależności pakietu.</span><span class="sxs-lookup"><span data-stu-id="e3262-180">`[DependencyName <String>]`: Name of package dependency.</span></span>
  - <span data-ttu-id="e3262-181">`[MinVersion <String>]`: Wymagana wersja zależności.</span><span class="sxs-lookup"><span data-stu-id="e3262-181">`[MinVersion <String>]`: Dependency version required.</span></span>
  - <span data-ttu-id="e3262-182">`[Publisher <String>]`: Nazwa wydawcy zależności.</span><span class="sxs-lookup"><span data-stu-id="e3262-182">`[Publisher <String>]`: Name of dependency publisher.</span></span>

## <span data-ttu-id="e3262-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3262-183">RELATED LINKS</span></span>

