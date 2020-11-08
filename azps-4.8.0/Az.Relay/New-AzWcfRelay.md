---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzWcfRelay.md
ms.openlocfilehash: 8fa9f3e2bbded846569609d9b1bae191d9f5ad89
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219278"
---
# <span data-ttu-id="fe545-101">New-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="fe545-101">New-AzWcfRelay</span></span>

## <span data-ttu-id="fe545-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fe545-102">SYNOPSIS</span></span>
<span data-ttu-id="fe545-103">Tworzy WcfRelay w określonym obszarze nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="fe545-103">Creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="fe545-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fe545-104">SYNTAX</span></span>

### <span data-ttu-id="fe545-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fe545-105">WcfRelayInputObjectSet</span></span>
```
New-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe545-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="fe545-106">WcfRelayPropertiesSet</span></span>
```
New-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-WcfRelayType <String>]
 [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>] [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe545-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fe545-107">DESCRIPTION</span></span>
<span data-ttu-id="fe545-108">Polecenie cmdlet New-AzWcfRelay tworzy WcfRelay w określonym obszarze nazw Relay.</span><span class="sxs-lookup"><span data-stu-id="fe545-108">The New-AzWcfRelay cmdlet creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="fe545-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fe545-109">EXAMPLES</span></span>

### <span data-ttu-id="fe545-110">Przykład 1-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fe545-110">Example 1 - InputObject</span></span>
```
PS C:\> $getWcfRelay = Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay1
PS C:\> $GetWcfRelay.UserMetadata = "TestWCFRelay2"
PS C:\> $GetWcfRelay.RequiresClientAuthorization = $False
PS C:\> $GetWcfRelay.RelayType = "Http"
PS C:\> New-AzWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay2 -InputObject

RelayType                   : Http
CreatedAt                   : 4/26/2017 5:14:46 PM
UpdatedAt                   : 4/26/2017 5:14:46 PM
ListenerCount               :
RequiresClientAuthorization : False
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : TestWCFRelay2
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2
Name                        : TestWCFRelay2
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="fe545-111">Tworzy nowy WcfRelay \` TestWCFRelay2 \` w określonym obszarze nazw przekaźnika \` TestNameSpace-Relay \` .</span><span class="sxs-lookup"><span data-stu-id="fe545-111">Creates a new WcfRelay \`TestWCFRelay2\` in the specified Relay namespace \`TestNameSpace-Relay\`.</span></span>

### <span data-ttu-id="fe545-112">Przykład 2-Properties</span><span class="sxs-lookup"><span data-stu-id="fe545-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay -WcfRelayType "NetTcp"  -RequiresClientAuthorization $True -RequiresTransportSecurity $True -UserMetadata "User Meta data"

RelayType                   : NetTcp
CreatedAt                   : 4/26/2017 5:20:08 PM
UpdatedAt                   : 4/26/2017 5:20:08 PM
ListenerCount               :
RequiresClientAuthorization : True
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
Name                        : TestWCFRelay
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="fe545-113">Tworzy nowy WcfRelay \` TestWCFRelay \` w określonym obszarze nazw Relay \` TestNameSpace-Relay1 \` .</span><span class="sxs-lookup"><span data-stu-id="fe545-113">Creates a new WcfRelay \`TestWCFRelay\` in the specified Relay namespace \`TestNameSpace-Relay1\`.</span></span>

## <span data-ttu-id="fe545-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fe545-114">PARAMETERS</span></span>

### <span data-ttu-id="fe545-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe545-115">-DefaultProfile</span></span>
<span data-ttu-id="fe545-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe545-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe545-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fe545-117">-InputObject</span></span>
<span data-ttu-id="fe545-118">Obiekt WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="fe545-118">WcfRelay object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe545-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fe545-119">-Name</span></span>
<span data-ttu-id="fe545-120">Nazwa WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="fe545-120">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe545-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fe545-121">-Namespace</span></span>
<span data-ttu-id="fe545-122">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="fe545-122">Namespace Name.</span></span>

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

### <span data-ttu-id="fe545-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="fe545-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="fe545-124">prawda, jeśli autoryzacja klienta jest wymagana dla tego przekazywania; w przeciwnym razie zwraca wartość FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="fe545-124">true if client authorization is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="fe545-125">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="fe545-125">-RequiresTransportSecurity</span></span>
<span data-ttu-id="fe545-126">prawda, jeśli dla tego przekazu jest potrzebne zabezpieczenie przed transportem; w przeciwnym razie zwraca wartość FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="fe545-126">true if transport security is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="fe545-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe545-127">-ResourceGroupName</span></span>
<span data-ttu-id="fe545-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fe545-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="fe545-129">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="fe545-129">-UserMetadata</span></span>
<span data-ttu-id="fe545-130">Pobiera lub ustawia usermetadata jest symbolem zastępczym, aby można było przechowywać dane ciągu zdefiniowanego przez użytkownika dla punktu końcowego HybridConnection. na przykład można go użyć do przechowywania danych opisujących, takich jak lista zespołów i informacji kontaktowych, również w celu przechowywania ustawień konfiguracji zdefiniowanych przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="fe545-130">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="fe545-131">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="fe545-131">-WcfRelayType</span></span>
<span data-ttu-id="fe545-132">Typ WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="fe545-132">WcfRelay Type.</span></span>
<span data-ttu-id="fe545-133">Możliwe wartości to: "NetTcp" lub "http".</span><span class="sxs-lookup"><span data-stu-id="fe545-133">Possible values include: 'NetTcp' or 'Http'</span></span>

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

### <span data-ttu-id="fe545-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fe545-134">-Confirm</span></span>
<span data-ttu-id="fe545-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe545-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe545-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe545-136">-WhatIf</span></span>
<span data-ttu-id="fe545-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe545-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe545-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fe545-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe545-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe545-139">CommonParameters</span></span>
<span data-ttu-id="fe545-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe545-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe545-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe545-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe545-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe545-142">INPUTS</span></span>

### <span data-ttu-id="fe545-143">System. String</span><span class="sxs-lookup"><span data-stu-id="fe545-143">System.String</span></span>

### <span data-ttu-id="fe545-144">Microsoft. Azure. Commands. Relay. modele. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="fe545-144">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

### <span data-ttu-id="fe545-145">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fe545-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="fe545-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fe545-146">OUTPUTS</span></span>

### <span data-ttu-id="fe545-147">Microsoft. Azure. Commands. Relay. modele. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="fe545-147">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="fe545-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fe545-148">NOTES</span></span>

## <span data-ttu-id="fe545-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe545-149">RELATED LINKS</span></span>
