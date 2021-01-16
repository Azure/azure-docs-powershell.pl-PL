---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: a7ff5c406cea050f809ef9ffa1e2d9974903fdc2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326088"
---
# <span data-ttu-id="63763-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="63763-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="63763-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="63763-102">SYNOPSIS</span></span>
<span data-ttu-id="63763-103">Usuwa regułę ograniczeń dostępu z aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="63763-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="63763-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="63763-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Action <String>] [-SlotName <String>] [-TargetScmSite] [-IpAddress <String>] [-SubnetName <String>]
 [-VirtualNetworkName <String>] [-SubnetId <String>] [-ServiceTag <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63763-105">Opis</span><span class="sxs-lookup"><span data-stu-id="63763-105">DESCRIPTION</span></span>
<span data-ttu-id="63763-106">Polecenie cmdlet **Remove-AzWebAppAccessRestrictionRule** usuwa regułę ograniczeń programu Access z aplikacji sieci Web platformy Azure</span><span class="sxs-lookup"><span data-stu-id="63763-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="63763-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="63763-107">EXAMPLES</span></span>

### <span data-ttu-id="63763-108">Przykład 1: Usuwanie reguły ograniczenia dostępu aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="63763-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="63763-109">To polecenie usuwa regułę ograniczenia dostępu IpRule z aplikacji Azure Web App o nazwie ContosoSite należącej do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="63763-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="63763-110">Przykład 2: Usuwanie reguły ograniczeń dostępu aplikacji sieci Web o znaczniku usługi</span><span class="sxs-lookup"><span data-stu-id="63763-110">Example 2: Remove a Service Tag Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="63763-111">To polecenie usuwa regułę ograniczeń programu Access z ServiceTag równą AzureFrontDoor. zaplecze z aplikacji Azure Web App o nazwie ContosoSite należącej do grupy zasobów o nazwie Default-Web-zachód.</span><span class="sxs-lookup"><span data-stu-id="63763-111">This command removes the access restriction rule with ServiceTag equals AzureFrontDoor.Backend from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="63763-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="63763-112">PARAMETERS</span></span>

### <span data-ttu-id="63763-113">-Action</span><span class="sxs-lookup"><span data-stu-id="63763-113">-Action</span></span>
<span data-ttu-id="63763-114">Reguła zezwalania lub odmowy.</span><span class="sxs-lookup"><span data-stu-id="63763-114">Allow or Deny rule.</span></span>

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

### <span data-ttu-id="63763-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63763-115">-DefaultProfile</span></span>
<span data-ttu-id="63763-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="63763-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63763-117">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="63763-117">-IpAddress</span></span>
<span data-ttu-id="63763-118">Adres IP z zakresu CIDR (wersja 4 lub 6).</span><span class="sxs-lookup"><span data-stu-id="63763-118">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="63763-119">Np.: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="63763-119">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="63763-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="63763-120">-Name</span></span>
<span data-ttu-id="63763-121">Nazwa reguły ograniczeń dostępu</span><span class="sxs-lookup"><span data-stu-id="63763-121">Access Restriction Rule Name</span></span>

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

### <span data-ttu-id="63763-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63763-122">-PassThru</span></span>
<span data-ttu-id="63763-123">Zwracanie obiektu konfiguracji ograniczenia dostępu.</span><span class="sxs-lookup"><span data-stu-id="63763-123">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="63763-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63763-124">-ResourceGroupName</span></span>
<span data-ttu-id="63763-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="63763-125">Resource Group Name</span></span>

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

### <span data-ttu-id="63763-126">-ServiceTag</span><span class="sxs-lookup"><span data-stu-id="63763-126">-ServiceTag</span></span>
<span data-ttu-id="63763-127">Nazwa numeru seryjny usługi</span><span class="sxs-lookup"><span data-stu-id="63763-127">Name of Service Tag</span></span>

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

### <span data-ttu-id="63763-128">-Slotname</span><span class="sxs-lookup"><span data-stu-id="63763-128">-SlotName</span></span>
<span data-ttu-id="63763-129">Nazwa miejsca wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="63763-129">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="63763-130">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="63763-130">-SubnetId</span></span>
<span data-ttu-id="63763-131">Identyfikator zasobu (ResourceId) podsieci.</span><span class="sxs-lookup"><span data-stu-id="63763-131">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="63763-132">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="63763-132">-SubnetName</span></span>
<span data-ttu-id="63763-133">Nazwa podsieci.</span><span class="sxs-lookup"><span data-stu-id="63763-133">Name of Subnet.</span></span>

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

### <span data-ttu-id="63763-134">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="63763-134">-TargetScmSite</span></span>
<span data-ttu-id="63763-135">Reguła ma na celu witrynę główną witryny lub SCM.</span><span class="sxs-lookup"><span data-stu-id="63763-135">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="63763-136">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="63763-136">-VirtualNetworkName</span></span>
<span data-ttu-id="63763-137">Nazwa sieci wirtualnej (musi się znajdować w tej samej grupie zasobów co aplikacja sieci Web).</span><span class="sxs-lookup"><span data-stu-id="63763-137">Name of Virtual Network (must be in same resource group as Web App).</span></span>

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

### <span data-ttu-id="63763-138">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="63763-138">-WebAppName</span></span>
<span data-ttu-id="63763-139">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="63763-139">The name of the web app.</span></span>

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

### <span data-ttu-id="63763-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="63763-140">-Confirm</span></span>
<span data-ttu-id="63763-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63763-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63763-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63763-142">-WhatIf</span></span>
<span data-ttu-id="63763-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63763-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63763-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="63763-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63763-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63763-145">CommonParameters</span></span>
<span data-ttu-id="63763-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63763-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63763-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63763-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63763-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63763-148">INPUTS</span></span>

### <span data-ttu-id="63763-149">System. String</span><span class="sxs-lookup"><span data-stu-id="63763-149">System.String</span></span>

## <span data-ttu-id="63763-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="63763-150">OUTPUTS</span></span>

### <span data-ttu-id="63763-151">Microsoft. Azure. Commands. webapps. modele. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="63763-151">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="63763-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="63763-152">NOTES</span></span>

## <span data-ttu-id="63763-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63763-153">RELATED LINKS</span></span>

[<span data-ttu-id="63763-154">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="63763-154">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="63763-155">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="63763-155">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="63763-156">Dodaj-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="63763-156">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)
