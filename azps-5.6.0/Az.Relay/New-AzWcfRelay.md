---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/new-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzWcfRelay.md
ms.openlocfilehash: 837c6e69f2b01ec0ae8de8ed7a711a041096dd2f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000474"
---
# <span data-ttu-id="cca49-101">New-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="cca49-101">New-AzWcfRelay</span></span>

## <span data-ttu-id="cca49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cca49-102">SYNOPSIS</span></span>
<span data-ttu-id="cca49-103">Tworzy WcfRelay w określonej przestrzeni nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="cca49-103">Creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="cca49-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cca49-104">SYNTAX</span></span>

### <span data-ttu-id="cca49-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cca49-105">WcfRelayInputObjectSet</span></span>
```
New-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cca49-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="cca49-106">WcfRelayPropertiesSet</span></span>
```
New-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-WcfRelayType <String>]
 [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>] [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cca49-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="cca49-107">DESCRIPTION</span></span>
<span data-ttu-id="cca49-108">Polecenie New-AzWcfRelay cmdlet tworzy WcfRelay w określonej przestrzeni nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="cca49-108">The New-AzWcfRelay cmdlet creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="cca49-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cca49-109">EXAMPLES</span></span>

### <span data-ttu-id="cca49-110">Przykład 1. InputObject</span><span class="sxs-lookup"><span data-stu-id="cca49-110">Example 1 - InputObject</span></span>
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

<span data-ttu-id="cca49-111">Tworzy nową nazwę WcfRelay TestWCFRelay2 w określonej przestrzeni nazw \` \` Relay \` TestNameSpace-Relay. \`</span><span class="sxs-lookup"><span data-stu-id="cca49-111">Creates a new WcfRelay \`TestWCFRelay2\` in the specified Relay namespace \`TestNameSpace-Relay\`.</span></span>

### <span data-ttu-id="cca49-112">Przykład 2. Właściwości</span><span class="sxs-lookup"><span data-stu-id="cca49-112">Example 2 - Properties</span></span>
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

<span data-ttu-id="cca49-113">Tworzy nową nazwę WcfRelay \` TestWCFRelay w określonej przestrzeni nazw \` \` Przekazywania TestNameSpace-Relay1. \`</span><span class="sxs-lookup"><span data-stu-id="cca49-113">Creates a new WcfRelay \`TestWCFRelay\` in the specified Relay namespace \`TestNameSpace-Relay1\`.</span></span>

## <span data-ttu-id="cca49-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cca49-114">PARAMETERS</span></span>

### <span data-ttu-id="cca49-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cca49-115">-DefaultProfile</span></span>
<span data-ttu-id="cca49-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cca49-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cca49-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cca49-117">-InputObject</span></span>
<span data-ttu-id="cca49-118">Obiekt WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="cca49-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="cca49-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cca49-119">-Name</span></span>
<span data-ttu-id="cca49-120">Nazwa aplikacji WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="cca49-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="cca49-121">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="cca49-121">-Namespace</span></span>
<span data-ttu-id="cca49-122">Nazwa przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="cca49-122">Namespace Name.</span></span>

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

### <span data-ttu-id="cca49-123">- WymagaClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="cca49-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="cca49-124">prawda, jeśli do tego przekazywania jest potrzebna autoryzacja klienta; w przeciwnym razie fałsz</span><span class="sxs-lookup"><span data-stu-id="cca49-124">true if client authorization is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="cca49-125">— WymagaTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="cca49-125">-RequiresTransportSecurity</span></span>
<span data-ttu-id="cca49-126">prawda, jeśli dla tego przekazywania jest wymagane bezpieczeństwo transportu; w przeciwnym razie fałsz</span><span class="sxs-lookup"><span data-stu-id="cca49-126">true if transport security is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="cca49-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cca49-127">-ResourceGroupName</span></span>
<span data-ttu-id="cca49-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cca49-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="cca49-129">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="cca49-129">-UserMetadata</span></span>
<span data-ttu-id="cca49-130">Pobiera lub ustawia dane użytkownika jest symbolem zastępczym do przechowywania danych ciągu zdefiniowanych przez użytkownika dla punktu końcowego połączenia hybrydowego, np. może być używana do przechowywania danych opisowych, takich jak lista zespołów i ich informacje kontaktowe, a także mogą być przechowywane ustawienia konfiguracji zdefiniowane przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cca49-130">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="cca49-131">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="cca49-131">-WcfRelayType</span></span>
<span data-ttu-id="cca49-132">Typ WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="cca49-132">WcfRelay Type.</span></span>
<span data-ttu-id="cca49-133">Możliwe wartości: "NetTcp" lub "Http"</span><span class="sxs-lookup"><span data-stu-id="cca49-133">Possible values include: 'NetTcp' or 'Http'</span></span>

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

### <span data-ttu-id="cca49-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cca49-134">-Confirm</span></span>
<span data-ttu-id="cca49-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cca49-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cca49-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cca49-136">-WhatIf</span></span>
<span data-ttu-id="cca49-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cca49-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cca49-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cca49-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cca49-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cca49-139">CommonParameters</span></span>
<span data-ttu-id="cca49-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cca49-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cca49-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cca49-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cca49-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cca49-142">INPUTS</span></span>

### <span data-ttu-id="cca49-143">System.String</span><span class="sxs-lookup"><span data-stu-id="cca49-143">System.String</span></span>

### <span data-ttu-id="cca49-144">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="cca49-144">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

### <span data-ttu-id="cca49-145">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cca49-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="cca49-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cca49-146">OUTPUTS</span></span>

### <span data-ttu-id="cca49-147">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="cca49-147">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="cca49-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cca49-148">NOTES</span></span>

## <span data-ttu-id="cca49-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cca49-149">RELATED LINKS</span></span>
