---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
ms.openlocfilehash: 04925f904861eea006c6480dbdb48794afc55c56
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708451"
---
# <span data-ttu-id="e976a-101">Set-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="e976a-101">Set-AzWcfRelay</span></span>

## <span data-ttu-id="e976a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e976a-102">SYNOPSIS</span></span>
<span data-ttu-id="e976a-103">Umożliwia zaktualizowanie opisu WcfRelay w określonej przestrzeni nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="e976a-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="e976a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e976a-104">SYNTAX</span></span>

### <span data-ttu-id="e976a-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e976a-105">WcfRelayInputObjectSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e976a-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="e976a-106">WcfRelayPropertiesSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e976a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e976a-107">DESCRIPTION</span></span>
<span data-ttu-id="e976a-108">Polecenie cmdlet Set-AzWcfRelay aktualizuje opis WcfRelay w określonej przestrzeni nazw Relay.</span><span class="sxs-lookup"><span data-stu-id="e976a-108">The Set-AzWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="e976a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e976a-109">EXAMPLES</span></span>

### <span data-ttu-id="e976a-110">Przykład 1-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e976a-110">Example 1 - InputObject</span></span>
```
PS C:\>
PS C:\> $getWcfRelay = Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay
PS C:\> $getWcfRelay.UserMetadata = "usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored."
PS C:\> Set-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -InputObject $getWcfRelay

RelayType                   : Http
CreatedAt                   : 4/26/2017 5:14:46 PM
UpdatedAt                   : 4/26/2017 5:16:50 PM
ListenerCount               :
RequiresClientAuthorization : False
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2
Name                        : TestWCFRelay2
Type                        : Microsoft.Relay/WcfRelays
```

### <span data-ttu-id="e976a-111">Przykład 2-Properties</span><span class="sxs-lookup"><span data-stu-id="e976a-111">Example 2 - Properties</span></span>
```
PS C:\> Set-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -UserMetadata "User Meta data"

RelayType                   : NetTcp
CreatedAt                   : 4/26/2017 5:20:08 PM
UpdatedAt                   : 4/26/2017 5:26:09 PM
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

<span data-ttu-id="e976a-112">Umożliwia zaktualizowanie określonego WcfRelay przy użyciu nowego opisu w określonym obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="e976a-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="e976a-113">W tym przykładzie zostanie zaktualizowana właściwość UserMetadata o nową wartość.</span><span class="sxs-lookup"><span data-stu-id="e976a-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="e976a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e976a-114">PARAMETERS</span></span>

### <span data-ttu-id="e976a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e976a-115">-DefaultProfile</span></span>
<span data-ttu-id="e976a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e976a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e976a-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e976a-117">-InputObject</span></span>
<span data-ttu-id="e976a-118">Obiekt WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="e976a-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="e976a-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e976a-119">-Name</span></span>
<span data-ttu-id="e976a-120">Nazwa WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="e976a-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="e976a-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e976a-121">-Namespace</span></span>
<span data-ttu-id="e976a-122">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="e976a-122">Namespace Name.</span></span>

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

### <span data-ttu-id="e976a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e976a-123">-ResourceGroupName</span></span>
<span data-ttu-id="e976a-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e976a-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="e976a-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="e976a-125">-UserMetadata</span></span>
<span data-ttu-id="e976a-126">Pobiera lub ustawia usermetadata jest symbolem zastępczym, aby można było przechowywać dane ciągu zdefiniowanego przez użytkownika dla punktu końcowego WcfRelay. na przykład można go użyć do przechowywania danych opisujących, takich jak lista zespołów i informacji kontaktowych, również w celu przechowywania ustawień konfiguracji zdefiniowanych przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e976a-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the WcfRelay endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="e976a-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e976a-127">-Confirm</span></span>
<span data-ttu-id="e976a-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e976a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e976a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e976a-129">-WhatIf</span></span>
<span data-ttu-id="e976a-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e976a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e976a-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e976a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e976a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e976a-132">CommonParameters</span></span>
<span data-ttu-id="e976a-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e976a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e976a-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e976a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e976a-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e976a-135">INPUTS</span></span>

### <span data-ttu-id="e976a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e976a-136">System.String</span></span>

### <span data-ttu-id="e976a-137">Microsoft. Azure. Commands. Relay. modele. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="e976a-137">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="e976a-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e976a-138">OUTPUTS</span></span>

### <span data-ttu-id="e976a-139">Microsoft. Azure. Commands. Relay. modele. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="e976a-139">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="e976a-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e976a-140">NOTES</span></span>

## <span data-ttu-id="e976a-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e976a-141">RELATED LINKS</span></span>
