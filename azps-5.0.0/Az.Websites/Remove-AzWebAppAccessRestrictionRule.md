---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: ad0bdc95ea3d582a2f8b6b6b1f8bc772c795352c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233724"
---
# <span data-ttu-id="dde9a-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="dde9a-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="dde9a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dde9a-102">SYNOPSIS</span></span>
<span data-ttu-id="dde9a-103">Usuwa regułę ograniczeń dostępu z aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="dde9a-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="dde9a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dde9a-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Action <String>] [-TargetScmSite] [-SlotName <String>] [-IpAddress <String>] [-SubnetName <String>]
 [-VirtualNetworkName <String>] [-SubnetId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dde9a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dde9a-105">DESCRIPTION</span></span>
<span data-ttu-id="dde9a-106">Polecenie cmdlet **Remove-AzWebAppAccessRestrictionRule** usuwa regułę ograniczeń programu Access z aplikacji sieci Web platformy Azure</span><span class="sxs-lookup"><span data-stu-id="dde9a-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="dde9a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dde9a-107">EXAMPLES</span></span>

### <span data-ttu-id="dde9a-108">Przykład 1: Usuwanie reguły ograniczenia dostępu aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="dde9a-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="dde9a-109">To polecenie usuwa regułę ograniczenia dostępu IpRule z aplikacji Azure Web App o nazwie ContosoSite należącej do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="dde9a-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="dde9a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dde9a-110">PARAMETERS</span></span>

### <span data-ttu-id="dde9a-111">-Action</span><span class="sxs-lookup"><span data-stu-id="dde9a-111">-Action</span></span>
<span data-ttu-id="dde9a-112">Reguła zezwalania lub odmowy.</span><span class="sxs-lookup"><span data-stu-id="dde9a-112">Allow or Deny rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: Allow
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dde9a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dde9a-113">-DefaultProfile</span></span>
<span data-ttu-id="dde9a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dde9a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dde9a-115">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="dde9a-115">-IpAddress</span></span>
<span data-ttu-id="dde9a-116">Adres IP z zakresu CIDR (wersja 4 lub 6).</span><span class="sxs-lookup"><span data-stu-id="dde9a-116">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="dde9a-117">Np.: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="dde9a-117">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="dde9a-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dde9a-118">-Name</span></span>
<span data-ttu-id="dde9a-119">Nazwa reguły ograniczeń dostępu</span><span class="sxs-lookup"><span data-stu-id="dde9a-119">Access Restriction Rule Name</span></span>

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

### <span data-ttu-id="dde9a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dde9a-120">-PassThru</span></span>
<span data-ttu-id="dde9a-121">Zwracanie obiektu konfiguracji ograniczenia dostępu.</span><span class="sxs-lookup"><span data-stu-id="dde9a-121">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="dde9a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dde9a-122">-ResourceGroupName</span></span>
<span data-ttu-id="dde9a-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="dde9a-123">Resource Group Name</span></span>

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

### <span data-ttu-id="dde9a-124">-Slotname</span><span class="sxs-lookup"><span data-stu-id="dde9a-124">-SlotName</span></span>
<span data-ttu-id="dde9a-125">Nazwa miejsca wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="dde9a-125">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="dde9a-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="dde9a-126">-SubnetId</span></span>
<span data-ttu-id="dde9a-127">Identyfikator zasobu (ResourceId) podsieci.</span><span class="sxs-lookup"><span data-stu-id="dde9a-127">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="dde9a-128">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="dde9a-128">-SubnetName</span></span>
<span data-ttu-id="dde9a-129">Nazwa podsieci.</span><span class="sxs-lookup"><span data-stu-id="dde9a-129">Name of Subnet.</span></span>

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

### <span data-ttu-id="dde9a-130">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="dde9a-130">-TargetScmSite</span></span>
<span data-ttu-id="dde9a-131">Reguła ma na celu witrynę główną witryny lub SCM.</span><span class="sxs-lookup"><span data-stu-id="dde9a-131">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="dde9a-132">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="dde9a-132">-VirtualNetworkName</span></span>
<span data-ttu-id="dde9a-133">Nazwa sieci wirtualnej (musi się znajdować w tej samej grupie zasobów co aplikacja sieci Web).</span><span class="sxs-lookup"><span data-stu-id="dde9a-133">Name of Virtual Network (must be in same resource group as Web App).</span></span>

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

### <span data-ttu-id="dde9a-134">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="dde9a-134">-WebAppName</span></span>
<span data-ttu-id="dde9a-135">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="dde9a-135">The name of the web app.</span></span>

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

### <span data-ttu-id="dde9a-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dde9a-136">-Confirm</span></span>
<span data-ttu-id="dde9a-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dde9a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dde9a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dde9a-138">-WhatIf</span></span>
<span data-ttu-id="dde9a-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dde9a-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dde9a-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dde9a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dde9a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dde9a-141">CommonParameters</span></span>
<span data-ttu-id="dde9a-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dde9a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dde9a-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dde9a-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dde9a-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dde9a-144">INPUTS</span></span>

### <span data-ttu-id="dde9a-145">System. String</span><span class="sxs-lookup"><span data-stu-id="dde9a-145">System.String</span></span>

## <span data-ttu-id="dde9a-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dde9a-146">OUTPUTS</span></span>

### <span data-ttu-id="dde9a-147">Microsoft. Azure. Commands. webapps. modele. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="dde9a-147">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="dde9a-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dde9a-148">NOTES</span></span>

## <span data-ttu-id="dde9a-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dde9a-149">RELATED LINKS</span></span>

[<span data-ttu-id="dde9a-150">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="dde9a-150">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="dde9a-151">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="dde9a-151">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="dde9a-152">Dodaj-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="dde9a-152">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)
