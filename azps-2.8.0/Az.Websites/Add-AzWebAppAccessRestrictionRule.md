---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: bbb68888634b53d333f1c085443db8b205773e06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888473"
---
# <span data-ttu-id="b0ea0-101">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="b0ea0-101">Add-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="b0ea0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b0ea0-102">SYNOPSIS</span></span>
<span data-ttu-id="b0ea0-103">Dodaje regułę programu Access restiction do aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b0ea0-103">Adds an Access Restiction rule to an Azure Web App.</span></span>

## <span data-ttu-id="b0ea0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b0ea0-104">SYNTAX</span></span>

### <span data-ttu-id="b0ea0-105">IpAddressParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b0ea0-105">IpAddressParameterSet (Default)</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> -Name <String>
 [-Description <String>] -Priority <UInt32> -Action <String> [-SlotName <String>] [-TargetScmSite]
 -IpAddress <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0ea0-106">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0ea0-106">SubnetNameParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> -Name <String>
 [-Description <String>] -Priority <UInt32> -Action <String> [-SlotName <String>] [-TargetScmSite]
 -SubnetName <String> -VirtualNetworkName <String> [-IgnoreMissingServiceEndpoint] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0ea0-107">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0ea0-107">SubnetIdParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> -Name <String>
 [-Description <String>] -Priority <UInt32> -Action <String> [-SlotName <String>] [-TargetScmSite]
 -SubnetId <String> [-IgnoreMissingServiceEndpoint] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0ea0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b0ea0-108">DESCRIPTION</span></span>
<span data-ttu-id="b0ea0-109">Polecenie cmdlet **Add-AzWebAppAccessRestrictionRule** umożliwia dodanie reguły ograniczeń dostępu do aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b0ea0-109">The **Add-AzWebAppAccessRestrictionRule** cmdlet adds an Access Restriction rule to an Azure Web App.</span></span>

## <span data-ttu-id="b0ea0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b0ea0-110">EXAMPLES</span></span>

### <span data-ttu-id="b0ea0-111">Przykład 1: Dodawanie do aplikacji sieci Web reguły ograniczenia dostępu IpAddress</span><span class="sxs-lookup"><span data-stu-id="b0ea0-111">Example 1: Add IpAddress Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name IpRule -Priority 200 -Action Allow -IpAddress 10.10.0.0/8
```

<span data-ttu-id="b0ea0-112">To polecenie umożliwia dodanie reguły ograniczeń programu Access z priorytetem 200 i zakresem IP do aplikacji sieci Web o nazwie ContosoSite należącej do domyślnego ustawienia Grupa zasobów — w sieci Web.</span><span class="sxs-lookup"><span data-stu-id="b0ea0-112">This command adds an access restriction rule with priority 200 and ip range to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="b0ea0-113">Przykład 2: Dodawanie reguły ograniczeń dostępu do punktu końcowego usługi podsieci do aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="b0ea0-113">Example 2: Add Subnet Service Endpoint Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name SubnetRule -Priority 300 -Action Allow -SubnetName appgw-subnet -VirtualNetworkName corp-vnet
```

<span data-ttu-id="b0ea0-114">To polecenie dodaje regułę ograniczeń programu Access z priorytetem 300 i z podsiecią appgw-Subnet w sieci Corp-VNET do aplikacji internetowej o nazwie ContosoSite należącej do grupy zasobów Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="b0ea0-114">This command adds an access restriction rule with priority 300 and with subnet appgw-subnet in corp-vnet to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="b0ea0-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b0ea0-115">PARAMETERS</span></span>

### <span data-ttu-id="b0ea0-116">-Action</span><span class="sxs-lookup"><span data-stu-id="b0ea0-116">-Action</span></span>
<span data-ttu-id="b0ea0-117">Reguła zezwalania lub odmowy.</span><span class="sxs-lookup"><span data-stu-id="b0ea0-117">Allow or Deny rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0ea0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0ea0-118">-DefaultProfile</span></span>
<span data-ttu-id="b0ea0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b0ea0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0ea0-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="b0ea0-120">-Description</span></span>
<span data-ttu-id="b0ea0-121">Opis ograniczenia dostępu.</span><span class="sxs-lookup"><span data-stu-id="b0ea0-121">Access Restriction description.</span></span>

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

### <span data-ttu-id="b0ea0-122">-IgnoreMissingServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0ea0-122">-IgnoreMissingServiceEndpoint</span></span>
<span data-ttu-id="b0ea0-123">Określ, czy należy sprawdzić poprawność rejestracji punktu końcowego usługi w podsieci.</span><span class="sxs-lookup"><span data-stu-id="b0ea0-123">Specify if Service Endpoint registration at Subnet should be validated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SubnetNameParameterSet, SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0ea0-124">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="b0ea0-124">-IpAddress</span></span>
<span data-ttu-id="b0ea0-125">Adres IP z zakresu CIDR (wersja 4 lub 6).</span><span class="sxs-lookup"><span data-stu-id="b0ea0-125">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="b0ea0-126">Np.: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="b0ea0-126">E.g.: 192.168.0.0/24</span></span>

```yaml
Type: System.String
Parameter Sets: IpAddressParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0ea0-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b0ea0-127">-Name</span></span>
<span data-ttu-id="b0ea0-128">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="b0ea0-128">Rule Name</span></span>

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

### <span data-ttu-id="b0ea0-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0ea0-129">-PassThru</span></span>
<span data-ttu-id="b0ea0-130">Zwracanie obiektu konfiguracji ograniczenia dostępu.</span><span class="sxs-lookup"><span data-stu-id="b0ea0-130">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="b0ea0-131">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="b0ea0-131">-Priority</span></span>
<span data-ttu-id="b0ea0-132">Priorytet ograniczenia dostępu.</span><span class="sxs-lookup"><span data-stu-id="b0ea0-132">Access Restriction priority.</span></span> <span data-ttu-id="b0ea0-133">Na przykład: 500.</span><span class="sxs-lookup"><span data-stu-id="b0ea0-133">E.g.: 500.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0ea0-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0ea0-134">-ResourceGroupName</span></span>
<span data-ttu-id="b0ea0-135">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b0ea0-135">Resource Group Name</span></span>

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

### <span data-ttu-id="b0ea0-136">-Slotname</span><span class="sxs-lookup"><span data-stu-id="b0ea0-136">-SlotName</span></span>
<span data-ttu-id="b0ea0-137">Nazwa miejsca wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="b0ea0-137">Deployment Slot name.</span></span>

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

### <span data-ttu-id="b0ea0-138">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b0ea0-138">-SubnetId</span></span>
<span data-ttu-id="b0ea0-139">Identyfikator zasobu (ResourceId) podsieci.</span><span class="sxs-lookup"><span data-stu-id="b0ea0-139">ResourceId of Subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0ea0-140">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="b0ea0-140">-SubnetName</span></span>
<span data-ttu-id="b0ea0-141">Nazwa podsieci.</span><span class="sxs-lookup"><span data-stu-id="b0ea0-141">Name of Subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0ea0-142">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="b0ea0-142">-TargetScmSite</span></span>
<span data-ttu-id="b0ea0-143">Reguła ma na celu witrynę główną witryny lub SCM.</span><span class="sxs-lookup"><span data-stu-id="b0ea0-143">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="b0ea0-144">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="b0ea0-144">-VirtualNetworkName</span></span>
<span data-ttu-id="b0ea0-145">Nazwa sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b0ea0-145">Name of Virtual Network.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0ea0-146">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="b0ea0-146">-WebAppName</span></span>
<span data-ttu-id="b0ea0-147">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="b0ea0-147">The name of the web app.</span></span>

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

### <span data-ttu-id="b0ea0-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b0ea0-148">-Confirm</span></span>
<span data-ttu-id="b0ea0-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0ea0-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0ea0-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0ea0-150">-WhatIf</span></span>
<span data-ttu-id="b0ea0-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0ea0-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0ea0-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b0ea0-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0ea0-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0ea0-153">CommonParameters</span></span>
<span data-ttu-id="b0ea0-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0ea0-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0ea0-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0ea0-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0ea0-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0ea0-156">INPUTS</span></span>

### <span data-ttu-id="b0ea0-157">System. String</span><span class="sxs-lookup"><span data-stu-id="b0ea0-157">System.String</span></span>

## <span data-ttu-id="b0ea0-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b0ea0-158">OUTPUTS</span></span>

### <span data-ttu-id="b0ea0-159">Microsoft. Azure. Commands. webapps. modele. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="b0ea0-159">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="b0ea0-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b0ea0-160">NOTES</span></span>

## <span data-ttu-id="b0ea0-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0ea0-161">RELATED LINKS</span></span>

[<span data-ttu-id="b0ea0-162">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="b0ea0-162">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="b0ea0-163">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="b0ea0-163">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="b0ea0-164">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="b0ea0-164">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
