---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: a7ff5c406cea050f809ef9ffa1e2d9974903fdc2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995821"
---
# <span data-ttu-id="71e65-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="71e65-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="71e65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71e65-102">SYNOPSIS</span></span>
<span data-ttu-id="71e65-103">Usuwa regułę ograniczeń dostępu z aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="71e65-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="71e65-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="71e65-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Action <String>] [-SlotName <String>] [-TargetScmSite] [-IpAddress <String>] [-SubnetName <String>]
 [-VirtualNetworkName <String>] [-SubnetId <String>] [-ServiceTag <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71e65-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="71e65-105">DESCRIPTION</span></span>
<span data-ttu-id="71e65-106">Polecenie **cmdlet Remove-AzWebAppAccessRestrictionRule** usuwa regułę ograniczeń dostępu z aplikacji Azure Web App</span><span class="sxs-lookup"><span data-stu-id="71e65-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="71e65-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="71e65-107">EXAMPLES</span></span>

### <span data-ttu-id="71e65-108">Przykład 1. Usuwanie reguły ograniczeń dostępu do aplikacji Sieci Web</span><span class="sxs-lookup"><span data-stu-id="71e65-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="71e65-109">To polecenie usuwa regułę ograniczeń dostępu IpRule z aplikacji Azure Web App o nazwie ContosoSite, która należy do grupy zasobów o nazwie Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="71e65-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="71e65-110">Przykład 2. Usuwanie reguły ograniczeń dostępu aplikacji sieci Web tagu usługi</span><span class="sxs-lookup"><span data-stu-id="71e65-110">Example 2: Remove a Service Tag Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="71e65-111">To polecenie usuwa regułę ograniczeń dostępu z wartością ServiceTag równą wartości AzureFrontDoor.Backend z aplikacji Azure Web App o nazwie ContosoSite, która należy do grupy zasobów o nazwie Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="71e65-111">This command removes the access restriction rule with ServiceTag equals AzureFrontDoor.Backend from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="71e65-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71e65-112">PARAMETERS</span></span>

### <span data-ttu-id="71e65-113">— Akcja</span><span class="sxs-lookup"><span data-stu-id="71e65-113">-Action</span></span>
<span data-ttu-id="71e65-114">Reguła Zezwalaj lub Odmów.</span><span class="sxs-lookup"><span data-stu-id="71e65-114">Allow or Deny rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e65-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71e65-115">-DefaultProfile</span></span>
<span data-ttu-id="71e65-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="71e65-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e65-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="71e65-117">-IpAddress</span></span>
<span data-ttu-id="71e65-118">Zakres cidru CIDR w adresie IP w wersji 4 lub v6.</span><span class="sxs-lookup"><span data-stu-id="71e65-118">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="71e65-119">Np.: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="71e65-119">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="71e65-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="71e65-120">-Name</span></span>
<span data-ttu-id="71e65-121">Nazwa reguły ograniczeń dostępu</span><span class="sxs-lookup"><span data-stu-id="71e65-121">Access Restriction Rule Name</span></span>

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

### <span data-ttu-id="71e65-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71e65-122">-PassThru</span></span>
<span data-ttu-id="71e65-123">Zwróć obiekt konfiguracji ograniczeń dostępu.</span><span class="sxs-lookup"><span data-stu-id="71e65-123">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="71e65-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71e65-124">-ResourceGroupName</span></span>
<span data-ttu-id="71e65-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="71e65-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e65-126">- ServiceTag</span><span class="sxs-lookup"><span data-stu-id="71e65-126">-ServiceTag</span></span>
<span data-ttu-id="71e65-127">Nazwa tagu usługi</span><span class="sxs-lookup"><span data-stu-id="71e65-127">Name of Service Tag</span></span>

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

### <span data-ttu-id="71e65-128">-SlotName</span><span class="sxs-lookup"><span data-stu-id="71e65-128">-SlotName</span></span>
<span data-ttu-id="71e65-129">Nazwa miejsca wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="71e65-129">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="71e65-130">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="71e65-130">-SubnetId</span></span>
<span data-ttu-id="71e65-131">ResourceId podsieci.</span><span class="sxs-lookup"><span data-stu-id="71e65-131">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="71e65-132">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="71e65-132">-SubnetName</span></span>
<span data-ttu-id="71e65-133">Nazwa podsieci.</span><span class="sxs-lookup"><span data-stu-id="71e65-133">Name of Subnet.</span></span>

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

### <span data-ttu-id="71e65-134">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="71e65-134">-TargetScmSite</span></span>
<span data-ttu-id="71e65-135">Reguła jest przeznaczona dla witryny głównej lub witryny scm.</span><span class="sxs-lookup"><span data-stu-id="71e65-135">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="71e65-136">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="71e65-136">-VirtualNetworkName</span></span>
<span data-ttu-id="71e65-137">Nazwa sieci wirtualnej (musi być w tej samej grupie zasobów, co aplikacja Web App).</span><span class="sxs-lookup"><span data-stu-id="71e65-137">Name of Virtual Network (must be in same resource group as Web App).</span></span>

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

### <span data-ttu-id="71e65-138">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="71e65-138">-WebAppName</span></span>
<span data-ttu-id="71e65-139">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="71e65-139">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e65-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="71e65-140">-Confirm</span></span>
<span data-ttu-id="71e65-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="71e65-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71e65-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71e65-142">-WhatIf</span></span>
<span data-ttu-id="71e65-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71e65-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71e65-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="71e65-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71e65-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e65-145">CommonParameters</span></span>
<span data-ttu-id="71e65-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71e65-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e65-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71e65-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e65-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71e65-148">INPUTS</span></span>

### <span data-ttu-id="71e65-149">System.String</span><span class="sxs-lookup"><span data-stu-id="71e65-149">System.String</span></span>

## <span data-ttu-id="71e65-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71e65-150">OUTPUTS</span></span>

### <span data-ttu-id="71e65-151">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="71e65-151">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="71e65-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="71e65-152">NOTES</span></span>

## <span data-ttu-id="71e65-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71e65-153">RELATED LINKS</span></span>

[<span data-ttu-id="71e65-154">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="71e65-154">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="71e65-155">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="71e65-155">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="71e65-156">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="71e65-156">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)
