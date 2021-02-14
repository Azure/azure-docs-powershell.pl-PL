---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: b28cb8ac408ff281930eac68bf2b97d288150dd6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188722"
---
# <span data-ttu-id="b3b4d-101">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="b3b4d-101">Add-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="b3b4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3b4d-102">SYNOPSIS</span></span>
<span data-ttu-id="b3b4d-103">Dodaje regułę Restiction programu Access do aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-103">Adds an Access Restiction rule to an Azure Web App.</span></span>

## <span data-ttu-id="b3b4d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b3b4d-104">SYNTAX</span></span>

### <span data-ttu-id="b3b4d-105">IpAddressParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b3b4d-105">IpAddressParameterSet (Default)</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -IpAddress <String> [-PassThru] [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3b4d-106">ServiceTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3b4d-106">ServiceTagParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 [-PassThru] -ServiceTag <String> [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3b4d-107">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3b4d-107">SubnetNameParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetName <String> -VirtualNetworkName <String> [-IgnoreMissingServiceEndpoint] [-PassThru]
 [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3b4d-108">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3b4d-108">SubnetIdParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetId <String> [-IgnoreMissingServiceEndpoint] [-PassThru] [-HttpHeader <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3b4d-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="b3b4d-109">DESCRIPTION</span></span>
<span data-ttu-id="b3b4d-110">Polecenie **cmdlet Add-AzWebAppAccessRestrictionRule** dodaje regułę ograniczeń dostępu do aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-110">The **Add-AzWebAppAccessRestrictionRule** cmdlet adds an Access Restriction rule to an Azure Web App.</span></span>

## <span data-ttu-id="b3b4d-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b3b4d-111">EXAMPLES</span></span>

### <span data-ttu-id="b3b4d-112">Przykład 1. Dodawanie reguły ograniczeń dostępu IpAddress do aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="b3b4d-112">Example 1: Add IpAddress Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name IpRule -Priority 200 -Action Allow -IpAddress 10.10.0.0/8
```

<span data-ttu-id="b3b4d-113">To polecenie dodaje regułę ograniczeń dostępu o priorytecie 200 i zakresie adresów IP do aplikacji Sieci Web o nazwie ContosoSite, która należy do grupy zasobów Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-113">This command adds an access restriction rule with priority 200 and ip range to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="b3b4d-114">Przykład 2. Dodawanie reguły ograniczeń dostępu punktu końcowego usługi podsieci do aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="b3b4d-114">Example 2: Add Subnet Service Endpoint Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name SubnetRule -Priority 300 -Action Allow -SubnetName appgw-subnet -VirtualNetworkName corp-vnet
```

<span data-ttu-id="b3b4d-115">To polecenie dodaje regułę ograniczeń dostępu o priorytecie 300 i z podsiecią podrzędną appgw-subnet w corp-vnet do aplikacji Sieci Web o nazwie ContosoSite, która należy do grupy zasobów Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-115">This command adds an access restriction rule with priority 300 and with subnet appgw-subnet in corp-vnet to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="b3b4d-116">Przykład 3. Dodawanie reguły ograniczeń dostępu do tagu serwisowego do aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="b3b4d-116">Example 3: Add ServiceTag Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name ServiceTagRule -Priority 200 -Action Allow -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="b3b4d-117">To polecenie dodaje regułę ograniczeń dostępu o priorytecie 200 oraz tag usługi reprezentujący zakres adresów IP usługi Front Door platformy Azure do aplikacji Sieci Web o nazwie ContosoSite, która należy do grupy zasobów Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-117">This command adds an access restriction rule with priority 200 and a Service Tag representing the ip scope of Azure Front Door to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="b3b4d-118">Przykład 4. Dodawanie wieloadresowej reguły ograniczeń dostępu do aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="b3b4d-118">Example 4: Add multi-address Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name MultipleIpRule -Priority 200 -Action Allow -IpAddress "10.10.0.0/8,192.168.0.0/16"
```

<span data-ttu-id="b3b4d-119">To polecenie dodaje regułę ograniczeń dostępu o priorytecie 200 i dwa zakresy adresów IP do aplikacji Sieci Web o nazwie ContosoSite, która należy do grupy zasobów Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-119">This command adds an access restriction rule with priority 200 and two ip ranges to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="b3b4d-120">Przykład 5. Dodawanie reguły ograniczeń dostępu z nagłówkiem http do aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="b3b4d-120">Example 5: Add Access Restriction rule with http header to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name MultipleIpRule -Priority 400 -Action Allow -ServiceTag AzureFrontDoor.Backend
-HttpHeader @{'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'; 'x-azure-fdid' = '355deb06-47c4-4ba4-9641-c7d7a98b913e'}
```

<span data-ttu-id="b3b4d-121">To polecenie dodaje regułę ograniczeń dostępu o priorytecie 400 dla tagu usługi AzureFrontDoor.Backend i dodatkowo ogranicza dostęp tylko do nagłówków http określonych wartości do aplikacji Sieci Web o nazwie ContosoSite, która należy do grupy zasobów Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-121">This command adds an access restriction rule with priority 400 for Service Tag AzureFrontDoor.Backend and further restricts access only to http headers of certain values to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="b3b4d-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3b4d-122">PARAMETERS</span></span>

### <span data-ttu-id="b3b4d-123">— akcja</span><span class="sxs-lookup"><span data-stu-id="b3b4d-123">-Action</span></span>
<span data-ttu-id="b3b4d-124">Reguła Zezwalaj lub Odmów.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-124">Allow or Deny rule.</span></span>

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

### <span data-ttu-id="b3b4d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3b4d-125">-DefaultProfile</span></span>
<span data-ttu-id="b3b4d-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3b4d-127">— Opis</span><span class="sxs-lookup"><span data-stu-id="b3b4d-127">-Description</span></span>
<span data-ttu-id="b3b4d-128">Opis ograniczeń dostępu.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-128">Access Restriction description.</span></span>

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

### <span data-ttu-id="b3b4d-129">- HttpHeader</span><span class="sxs-lookup"><span data-stu-id="b3b4d-129">-HttpHeader</span></span>
<span data-ttu-id="b3b4d-130">Ograniczenia nagłówka HTTP.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-130">Http header restrictions.</span></span> <span data-ttu-id="b3b4d-131">Przykład: -HttpHeader @{'x-azure-fdid' = '7acacb02-47ea-4cd4-b568-5e880e72582e'; 'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'}</span><span class="sxs-lookup"><span data-stu-id="b3b4d-131">Example: -HttpHeader @{'x-azure-fdid' = '7acacb02-47ea-4cd4-b568-5e880e72582e'; 'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b4d-132">-IgnoreMissingServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="b3b4d-132">-IgnoreMissingServiceEndpoint</span></span>
<span data-ttu-id="b3b4d-133">Określ, czy należy sprawdzić poprawność rejestracji punktu końcowego usługi w podsieci.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-133">Specify if Service Endpoint registration at Subnet should be validated.</span></span>

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

### <span data-ttu-id="b3b4d-134">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="b3b4d-134">-IpAddress</span></span>
<span data-ttu-id="b3b4d-135">Zakres cidru CIDR w adresie IP w wersji 4 lub v6.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-135">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="b3b4d-136">Np.: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="b3b4d-136">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="b3b4d-137">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b3b4d-137">-Name</span></span>
<span data-ttu-id="b3b4d-138">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="b3b4d-138">Rule Name</span></span>

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

### <span data-ttu-id="b3b4d-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3b4d-139">-PassThru</span></span>
<span data-ttu-id="b3b4d-140">Zwróć obiekt konfiguracji ograniczeń dostępu.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-140">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="b3b4d-141">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="b3b4d-141">-Priority</span></span>
<span data-ttu-id="b3b4d-142">Priorytet ograniczeń dostępu.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-142">Access Restriction priority.</span></span> <span data-ttu-id="b3b4d-143">Np.: 500.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-143">E.g.: 500.</span></span>

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

### <span data-ttu-id="b3b4d-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3b4d-144">-ResourceGroupName</span></span>
<span data-ttu-id="b3b4d-145">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b3b4d-145">Resource Group Name</span></span>

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

### <span data-ttu-id="b3b4d-146">- ServiceTag</span><span class="sxs-lookup"><span data-stu-id="b3b4d-146">-ServiceTag</span></span>
<span data-ttu-id="b3b4d-147">Nazwa tagu usługi</span><span class="sxs-lookup"><span data-stu-id="b3b4d-147">Name of Service Tag</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceTagParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b4d-148">-SlotName</span><span class="sxs-lookup"><span data-stu-id="b3b4d-148">-SlotName</span></span>
<span data-ttu-id="b3b4d-149">Nazwa miejsca wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-149">Deployment Slot name.</span></span>

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

### <span data-ttu-id="b3b4d-150">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b3b4d-150">-SubnetId</span></span>
<span data-ttu-id="b3b4d-151">ResourceId podsieci.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-151">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="b3b4d-152">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="b3b4d-152">-SubnetName</span></span>
<span data-ttu-id="b3b4d-153">Nazwa podsieci.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-153">Name of Subnet.</span></span>

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

### <span data-ttu-id="b3b4d-154">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="b3b4d-154">-TargetScmSite</span></span>
<span data-ttu-id="b3b4d-155">Reguła jest przeznaczona dla witryny głównej lub witryny scm.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-155">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="b3b4d-156">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="b3b4d-156">-VirtualNetworkName</span></span>
<span data-ttu-id="b3b4d-157">Nazwa sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-157">Name of Virtual Network.</span></span>

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

### <span data-ttu-id="b3b4d-158">- WebAppName</span><span class="sxs-lookup"><span data-stu-id="b3b4d-158">-WebAppName</span></span>
<span data-ttu-id="b3b4d-159">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-159">The name of the web app.</span></span>

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

### <span data-ttu-id="b3b4d-160">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b3b4d-160">-Confirm</span></span>
<span data-ttu-id="b3b4d-161">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3b4d-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3b4d-162">-WhatIf</span></span>
<span data-ttu-id="b3b4d-163">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3b4d-164">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3b4d-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3b4d-165">CommonParameters</span></span>
<span data-ttu-id="b3b4d-166">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3b4d-167">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3b4d-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3b4d-168">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3b4d-168">INPUTS</span></span>

### <span data-ttu-id="b3b4d-169">System.String</span><span class="sxs-lookup"><span data-stu-id="b3b4d-169">System.String</span></span>

## <span data-ttu-id="b3b4d-170">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b3b4d-170">OUTPUTS</span></span>

### <span data-ttu-id="b3b4d-171">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="b3b4d-171">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="b3b4d-172">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b3b4d-172">NOTES</span></span>

## <span data-ttu-id="b3b4d-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3b4d-173">RELATED LINKS</span></span>

[<span data-ttu-id="b3b4d-174">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="b3b4d-174">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="b3b4d-175">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="b3b4d-175">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="b3b4d-176">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="b3b4d-176">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
