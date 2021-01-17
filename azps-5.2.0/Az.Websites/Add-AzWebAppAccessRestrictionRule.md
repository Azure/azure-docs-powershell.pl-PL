---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: b28cb8ac408ff281930eac68bf2b97d288150dd6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354721"
---
# <span data-ttu-id="af733-101">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="af733-101">Add-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="af733-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="af733-102">SYNOPSIS</span></span>
<span data-ttu-id="af733-103">Dodaje regułę programu Access restiction do aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="af733-103">Adds an Access Restiction rule to an Azure Web App.</span></span>

## <span data-ttu-id="af733-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="af733-104">SYNTAX</span></span>

### <span data-ttu-id="af733-105">IpAddressParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="af733-105">IpAddressParameterSet (Default)</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -IpAddress <String> [-PassThru] [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af733-106">ServiceTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="af733-106">ServiceTagParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 [-PassThru] -ServiceTag <String> [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af733-107">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="af733-107">SubnetNameParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetName <String> -VirtualNetworkName <String> [-IgnoreMissingServiceEndpoint] [-PassThru]
 [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af733-108">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="af733-108">SubnetIdParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetId <String> [-IgnoreMissingServiceEndpoint] [-PassThru] [-HttpHeader <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af733-109">Opis</span><span class="sxs-lookup"><span data-stu-id="af733-109">DESCRIPTION</span></span>
<span data-ttu-id="af733-110">Polecenie cmdlet **Add-AzWebAppAccessRestrictionRule** umożliwia dodanie reguły ograniczeń dostępu do aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="af733-110">The **Add-AzWebAppAccessRestrictionRule** cmdlet adds an Access Restriction rule to an Azure Web App.</span></span>

## <span data-ttu-id="af733-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="af733-111">EXAMPLES</span></span>

### <span data-ttu-id="af733-112">Przykład 1: Dodawanie do aplikacji sieci Web reguły ograniczenia dostępu IpAddress</span><span class="sxs-lookup"><span data-stu-id="af733-112">Example 1: Add IpAddress Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name IpRule -Priority 200 -Action Allow -IpAddress 10.10.0.0/8
```

<span data-ttu-id="af733-113">To polecenie umożliwia dodanie reguły ograniczeń programu Access z priorytetem 200 i zakresem IP do aplikacji sieci Web o nazwie ContosoSite należącej do domyślnego ustawienia Grupa zasobów — w sieci Web.</span><span class="sxs-lookup"><span data-stu-id="af733-113">This command adds an access restriction rule with priority 200 and ip range to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="af733-114">Przykład 2: Dodawanie reguły ograniczeń dostępu do punktu końcowego usługi podsieci do aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="af733-114">Example 2: Add Subnet Service Endpoint Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name SubnetRule -Priority 300 -Action Allow -SubnetName appgw-subnet -VirtualNetworkName corp-vnet
```

<span data-ttu-id="af733-115">To polecenie dodaje regułę ograniczeń programu Access z priorytetem 300 i z podsiecią appgw-Subnet w sieci Corp-VNET do aplikacji internetowej o nazwie ContosoSite należącej do grupy zasobów Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="af733-115">This command adds an access restriction rule with priority 300 and with subnet appgw-subnet in corp-vnet to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="af733-116">Przykład 3: Dodawanie reguły ograniczeń dostępu ServiceTag do aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="af733-116">Example 3: Add ServiceTag Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name ServiceTagRule -Priority 200 -Action Allow -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="af733-117">To polecenie dodaje regułę ograniczeń dostępu z priorytetem 200 i znacznikiem usługi reprezentującym zakres adresów IP frontonu platformy Azure do aplikacji sieci Web o nazwie ContosoSite należącej do ustawień domyślnych grupy zasobów — w sieci Web.</span><span class="sxs-lookup"><span data-stu-id="af733-117">This command adds an access restriction rule with priority 200 and a Service Tag representing the ip scope of Azure Front Door to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="af733-118">Przykład 4: Dodawanie reguły ograniczeń dostępu z wieloma adresami do aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="af733-118">Example 4: Add multi-address Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name MultipleIpRule -Priority 200 -Action Allow -IpAddress "10.10.0.0/8,192.168.0.0/16"
```

<span data-ttu-id="af733-119">To polecenie umożliwia dodanie reguły ograniczeń programu Access z priorytetem 200 i dwoma zakresami IP do aplikacji sieci Web o nazwie ContosoSite należącej do grupy zasobów Default — Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="af733-119">This command adds an access restriction rule with priority 200 and two ip ranges to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="af733-120">Przykład 5: Dodawanie reguły ograniczeń dostępu z nagłówkiem http do aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="af733-120">Example 5: Add Access Restriction rule with http header to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name MultipleIpRule -Priority 400 -Action Allow -ServiceTag AzureFrontDoor.Backend
-HttpHeader @{'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'; 'x-azure-fdid' = '355deb06-47c4-4ba4-9641-c7d7a98b913e'}
```

<span data-ttu-id="af733-121">To polecenie umożliwia dodanie reguły ograniczeń programu Access z priorytetem 400 dla programu Service Tag AzureFrontDoor. wewnętrzna baza danych, która dodatkowo ogranicza dostęp tylko do nagłówków HTTP określonych wartości do aplikacji sieci Web o nazwie ContosoSite należącej do grupy zasobów Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="af733-121">This command adds an access restriction rule with priority 400 for Service Tag AzureFrontDoor.Backend and further restricts access only to http headers of certain values to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="af733-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="af733-122">PARAMETERS</span></span>

### <span data-ttu-id="af733-123">-Action</span><span class="sxs-lookup"><span data-stu-id="af733-123">-Action</span></span>
<span data-ttu-id="af733-124">Reguła zezwalania lub odmowy.</span><span class="sxs-lookup"><span data-stu-id="af733-124">Allow or Deny rule.</span></span>

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

### <span data-ttu-id="af733-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af733-125">-DefaultProfile</span></span>
<span data-ttu-id="af733-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="af733-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af733-127">— Opis</span><span class="sxs-lookup"><span data-stu-id="af733-127">-Description</span></span>
<span data-ttu-id="af733-128">Opis ograniczenia dostępu.</span><span class="sxs-lookup"><span data-stu-id="af733-128">Access Restriction description.</span></span>

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

### <span data-ttu-id="af733-129">-HttpHeader</span><span class="sxs-lookup"><span data-stu-id="af733-129">-HttpHeader</span></span>
<span data-ttu-id="af733-130">Ograniczenia nagłówka HTTP.</span><span class="sxs-lookup"><span data-stu-id="af733-130">Http header restrictions.</span></span> <span data-ttu-id="af733-131">Przykład:-HttpHeader @ {' x-Azure-fdid ' = ' 7acacb02-47EA-4cd4-b568-5e880e72582e '; "x-przesłane dalej-host" = "www.contoso.com", "app.contoso.com"}</span><span class="sxs-lookup"><span data-stu-id="af733-131">Example: -HttpHeader @{'x-azure-fdid' = '7acacb02-47ea-4cd4-b568-5e880e72582e'; 'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'}</span></span>

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

### <span data-ttu-id="af733-132">-IgnoreMissingServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="af733-132">-IgnoreMissingServiceEndpoint</span></span>
<span data-ttu-id="af733-133">Określ, czy należy sprawdzić poprawność rejestracji punktu końcowego usługi w podsieci.</span><span class="sxs-lookup"><span data-stu-id="af733-133">Specify if Service Endpoint registration at Subnet should be validated.</span></span>

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

### <span data-ttu-id="af733-134">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="af733-134">-IpAddress</span></span>
<span data-ttu-id="af733-135">Adres IP z zakresu CIDR (wersja 4 lub 6).</span><span class="sxs-lookup"><span data-stu-id="af733-135">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="af733-136">Np.: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="af733-136">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="af733-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="af733-137">-Name</span></span>
<span data-ttu-id="af733-138">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="af733-138">Rule Name</span></span>

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

### <span data-ttu-id="af733-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af733-139">-PassThru</span></span>
<span data-ttu-id="af733-140">Zwracanie obiektu konfiguracji ograniczenia dostępu.</span><span class="sxs-lookup"><span data-stu-id="af733-140">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="af733-141">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="af733-141">-Priority</span></span>
<span data-ttu-id="af733-142">Priorytet ograniczenia dostępu.</span><span class="sxs-lookup"><span data-stu-id="af733-142">Access Restriction priority.</span></span> <span data-ttu-id="af733-143">Na przykład: 500.</span><span class="sxs-lookup"><span data-stu-id="af733-143">E.g.: 500.</span></span>

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

### <span data-ttu-id="af733-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af733-144">-ResourceGroupName</span></span>
<span data-ttu-id="af733-145">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="af733-145">Resource Group Name</span></span>

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

### <span data-ttu-id="af733-146">-ServiceTag</span><span class="sxs-lookup"><span data-stu-id="af733-146">-ServiceTag</span></span>
<span data-ttu-id="af733-147">Nazwa numeru seryjny usługi</span><span class="sxs-lookup"><span data-stu-id="af733-147">Name of Service Tag</span></span>

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

### <span data-ttu-id="af733-148">-Slotname</span><span class="sxs-lookup"><span data-stu-id="af733-148">-SlotName</span></span>
<span data-ttu-id="af733-149">Nazwa miejsca wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="af733-149">Deployment Slot name.</span></span>

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

### <span data-ttu-id="af733-150">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="af733-150">-SubnetId</span></span>
<span data-ttu-id="af733-151">Identyfikator zasobu (ResourceId) podsieci.</span><span class="sxs-lookup"><span data-stu-id="af733-151">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="af733-152">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="af733-152">-SubnetName</span></span>
<span data-ttu-id="af733-153">Nazwa podsieci.</span><span class="sxs-lookup"><span data-stu-id="af733-153">Name of Subnet.</span></span>

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

### <span data-ttu-id="af733-154">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="af733-154">-TargetScmSite</span></span>
<span data-ttu-id="af733-155">Reguła ma na celu witrynę główną witryny lub SCM.</span><span class="sxs-lookup"><span data-stu-id="af733-155">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="af733-156">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="af733-156">-VirtualNetworkName</span></span>
<span data-ttu-id="af733-157">Nazwa sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="af733-157">Name of Virtual Network.</span></span>

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

### <span data-ttu-id="af733-158">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="af733-158">-WebAppName</span></span>
<span data-ttu-id="af733-159">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="af733-159">The name of the web app.</span></span>

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

### <span data-ttu-id="af733-160">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="af733-160">-Confirm</span></span>
<span data-ttu-id="af733-161">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af733-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af733-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af733-162">-WhatIf</span></span>
<span data-ttu-id="af733-163">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af733-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af733-164">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="af733-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af733-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af733-165">CommonParameters</span></span>
<span data-ttu-id="af733-166">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af733-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af733-167">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af733-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af733-168">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af733-168">INPUTS</span></span>

### <span data-ttu-id="af733-169">System. String</span><span class="sxs-lookup"><span data-stu-id="af733-169">System.String</span></span>

## <span data-ttu-id="af733-170">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="af733-170">OUTPUTS</span></span>

### <span data-ttu-id="af733-171">Microsoft. Azure. Commands. webapps. modele. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="af733-171">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="af733-172">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="af733-172">NOTES</span></span>

## <span data-ttu-id="af733-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af733-173">RELATED LINKS</span></span>

[<span data-ttu-id="af733-174">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="af733-174">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="af733-175">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="af733-175">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="af733-176">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="af733-176">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
