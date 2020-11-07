---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
ms.openlocfilehash: a7a8734395b08c906b84cc4465528434fcb31eb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718103"
---
# <span data-ttu-id="25396-101">New-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="25396-101">New-AzureRmWcfRelay</span></span>

## <span data-ttu-id="25396-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="25396-102">SYNOPSIS</span></span>
<span data-ttu-id="25396-103">Tworzy WcfRelay w określonym obszarze nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="25396-103">Creates a WcfRelay in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25396-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="25396-104">SYNTAX</span></span>

### <span data-ttu-id="25396-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="25396-105">WcfRelayInputObjectSet</span></span>
```
New-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25396-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="25396-106">WcfRelayPropertiesSet</span></span>
```
New-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String> [-WcfRelayType <String>]
 [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>] [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25396-107">Opis</span><span class="sxs-lookup"><span data-stu-id="25396-107">DESCRIPTION</span></span>
<span data-ttu-id="25396-108">Polecenie cmdlet New-AzureRmWcfRelay tworzy WcfRelay w określonym obszarze nazw Relay.</span><span class="sxs-lookup"><span data-stu-id="25396-108">The New-AzureRmWcfRelay cmdlet creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="25396-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="25396-109">EXAMPLES</span></span>

### <span data-ttu-id="25396-110">Przykład 1-Inputobject</span><span class="sxs-lookup"><span data-stu-id="25396-110">Example 1 - InputObject</span></span>
```
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay1
PS C:\> $GetWcfRelay.UserMetadata = "TestWCFRelay2"
PS C:\> $GetWcfRelay.RequiresClientAuthorization = $False
PS C:\> $GetWcfRelay.RelayType = "Http"
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay2 -InputObject
```

<span data-ttu-id="25396-111">Tworzy nowy WcfRelay \` TestWCFRelay2 \` w określonym obszarze nazw przekaźnika \` TestNameSpace-Relay \` .</span><span class="sxs-lookup"><span data-stu-id="25396-111">Creates a new WcfRelay \`TestWCFRelay2\` in the specified Relay namespace \`TestNameSpace-Relay\`.</span></span>

### <span data-ttu-id="25396-112">Przykład 2-Properties</span><span class="sxs-lookup"><span data-stu-id="25396-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay -WcfRelayType "NetTcp"  -RequiresClientAuthorization $True -RequiresTransportSecurity $True -UserMetadata "User Meta data"
```

<span data-ttu-id="25396-113">Tworzy nowy WcfRelay \` TestWCFRelay \` w określonym obszarze nazw Relay \` TestNameSpace-Relay1 \` .</span><span class="sxs-lookup"><span data-stu-id="25396-113">Creates a new WcfRelay \`TestWCFRelay\` in the specified Relay namespace \`TestNameSpace-Relay1\`.</span></span>

## <span data-ttu-id="25396-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="25396-114">PARAMETERS</span></span>

### <span data-ttu-id="25396-115">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="25396-115">-RequiresClientAuthorization</span></span>
<span data-ttu-id="25396-116">prawda, jeśli autoryzacja klienta jest wymagana dla tego przekazywania; w przeciwnym razie zwraca wartość FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="25396-116">true if client authorization is needed for this relay; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25396-117">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="25396-117">-RequiresTransportSecurity</span></span>
<span data-ttu-id="25396-118">prawda, jeśli dla tego przekazu jest potrzebne zabezpieczenie przed transportem; w przeciwnym razie zwraca wartość FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="25396-118">true if transport security is needed for this relay; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25396-119">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="25396-119">-UserMetadata</span></span>
<span data-ttu-id="25396-120">Pobiera lub ustawia usermetadata jest symbolem zastępczym, aby można było przechowywać dane ciągu zdefiniowanego przez użytkownika dla punktu końcowego HybridConnection. na przykład można go użyć do przechowywania danych opisujących, takich jak lista zespołów i informacji kontaktowych, również w celu przechowywania ustawień konfiguracji zdefiniowanych przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="25396-120">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25396-121">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="25396-121">-WcfRelayType</span></span>
<span data-ttu-id="25396-122">Typ WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="25396-122">WcfRelay Type.</span></span>
<span data-ttu-id="25396-123">Możliwe wartości to: "NetTcp" lub "http".</span><span class="sxs-lookup"><span data-stu-id="25396-123">Possible values include: 'NetTcp' or 'Http'</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayPropertiesSet
Aliases: 
Accepted values: NetTcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25396-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="25396-124">-Confirm</span></span>
<span data-ttu-id="25396-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25396-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25396-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25396-126">-WhatIf</span></span>
<span data-ttu-id="25396-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25396-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25396-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="25396-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25396-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="25396-129">-InputObject</span></span>
<span data-ttu-id="25396-130">Obiekt WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="25396-130">WcfRelay object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25396-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="25396-131">-Name</span></span>
<span data-ttu-id="25396-132">Nazwa WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="25396-132">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25396-133">-Namespace</span><span class="sxs-lookup"><span data-stu-id="25396-133">-Namespace</span></span>
<span data-ttu-id="25396-134">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="25396-134">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25396-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25396-135">-ResourceGroupName</span></span>
<span data-ttu-id="25396-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="25396-136">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25396-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25396-137">-DefaultProfile</span></span>
<span data-ttu-id="25396-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="25396-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25396-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25396-139">CommonParameters</span></span>
<span data-ttu-id="25396-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25396-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25396-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25396-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25396-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25396-142">INPUTS</span></span>

### <span data-ttu-id="25396-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25396-143">-ResourceGroupName</span></span>
<span data-ttu-id="25396-144">System. String</span><span class="sxs-lookup"><span data-stu-id="25396-144">System.String</span></span>

### <span data-ttu-id="25396-145">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="25396-145">-NamespaceName</span></span>
<span data-ttu-id="25396-146">System. String</span><span class="sxs-lookup"><span data-stu-id="25396-146">System.String</span></span>

### <span data-ttu-id="25396-147">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="25396-147">-WcfRelayName</span></span>
<span data-ttu-id="25396-148">System. String</span><span class="sxs-lookup"><span data-stu-id="25396-148">System.String</span></span>

### <span data-ttu-id="25396-149">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="25396-149">-InputObject</span></span>
<span data-ttu-id="25396-150">Microsoft. Azure. Commands. Relay. modele. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="25396-150">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="25396-151">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="25396-151">-WcfRelayType</span></span>
<span data-ttu-id="25396-152">System. String</span><span class="sxs-lookup"><span data-stu-id="25396-152">System.String</span></span>

### <span data-ttu-id="25396-153">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="25396-153">-RequiresClientAuthorization</span></span>
<span data-ttu-id="25396-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25396-154">System.Boolean</span></span>

### <span data-ttu-id="25396-155">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="25396-155">-RequiresTransportSecurity</span></span>
<span data-ttu-id="25396-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25396-156">System.Boolean</span></span>

### <span data-ttu-id="25396-157">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="25396-157">-UserMetadata</span></span>
<span data-ttu-id="25396-158">System. String</span><span class="sxs-lookup"><span data-stu-id="25396-158">System.String</span></span>

## <span data-ttu-id="25396-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="25396-159">OUTPUTS</span></span>

### <span data-ttu-id="25396-160">Przykład 1-Inputobject</span><span class="sxs-lookup"><span data-stu-id="25396-160">Example 1 - InputObject</span></span>

### <span data-ttu-id="25396-161">Microsoft. Azure. Commands. Relay. modele. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="25396-161">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="25396-162">Relaytype: http CreatedAt: 4/26/2017 5:14:46 PM UpdatedAt: 4/26/2017 5:14:46 PM ListenerCount: RequiresClientAuthorization: false RequiresTransportSecurity: prawda IsDynamic: false UserMetadata: TestWCFRelay2 ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel dni/Namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name: TestWCFRelay2 Type: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="25396-162">RelayType                   : Http CreatedAt                   : 4/26/2017 5:14:46 PM UpdatedAt                   : 4/26/2017 5:14:46 PM ListenerCount               : RequiresClientAuthorization : False RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : TestWCFRelay2 Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name                        : TestWCFRelay2 Type                        : Microsoft.Relay/WcfRelays</span></span>

### <span data-ttu-id="25396-163">Przykład 2-Properties</span><span class="sxs-lookup"><span data-stu-id="25396-163">Example 2 - Properties</span></span>

### <span data-ttu-id="25396-164">Microsoft. Azure. Commands. Relay. modele. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="25396-164">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="25396-165">Relaytype: NetTcp CreatedAt: 4/26/2017 5:20:08 PM UpdatedAt: 4/26/2017 5:20:08 PM ListenerCount: RequiresClientAuthorization: prawda RequiresTransportSecurity: prawda IsDynamic: false UserMetadata: Identyfikator meta danych użytkownika:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel dni/obszary nazw/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name: TestWCFRelay Type: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="25396-165">RelayType                   : NetTcp CreatedAt                   : 4/26/2017 5:20:08 PM UpdatedAt                   : 4/26/2017 5:20:08 PM ListenerCount               : RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name                        : TestWCFRelay Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="25396-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="25396-166">NOTES</span></span>

## <span data-ttu-id="25396-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25396-167">RELATED LINKS</span></span>

