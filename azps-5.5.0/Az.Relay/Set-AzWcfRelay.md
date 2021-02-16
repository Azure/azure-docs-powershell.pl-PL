---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
ms.openlocfilehash: f7671d35901705ef96f6c1bf13c487c688a6214c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186531"
---
# <span data-ttu-id="c3480-101">Set-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="c3480-101">Set-AzWcfRelay</span></span>

## <span data-ttu-id="c3480-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3480-102">SYNOPSIS</span></span>
<span data-ttu-id="c3480-103">Aktualizuje opis pliku WcfRelay w określonej przestrzeni nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="c3480-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="c3480-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c3480-104">SYNTAX</span></span>

### <span data-ttu-id="c3480-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c3480-105">WcfRelayInputObjectSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3480-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="c3480-106">WcfRelayPropertiesSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3480-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c3480-107">DESCRIPTION</span></span>
<span data-ttu-id="c3480-108">Polecenie Set-AzWcfRelay aktualizuje opis pliku WcfRelay w określonej przestrzeni nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="c3480-108">The Set-AzWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="c3480-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c3480-109">EXAMPLES</span></span>

### <span data-ttu-id="c3480-110">Przykład 1. InputObject</span><span class="sxs-lookup"><span data-stu-id="c3480-110">Example 1 - InputObject</span></span>
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

### <span data-ttu-id="c3480-111">Przykład 2. Właściwości</span><span class="sxs-lookup"><span data-stu-id="c3480-111">Example 2 - Properties</span></span>
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

<span data-ttu-id="c3480-112">Aktualizuje określoną nazwę WcfRelay przy użyciu nowego opisu w określonej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="c3480-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="c3480-113">W tym przykładzie właściwość UserMetadata jest aktualizowana przy użyciu nowej wartości.</span><span class="sxs-lookup"><span data-stu-id="c3480-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="c3480-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3480-114">PARAMETERS</span></span>

### <span data-ttu-id="c3480-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3480-115">-DefaultProfile</span></span>
<span data-ttu-id="c3480-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3480-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3480-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3480-117">-InputObject</span></span>
<span data-ttu-id="c3480-118">Obiekt WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="c3480-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="c3480-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c3480-119">-Name</span></span>
<span data-ttu-id="c3480-120">Nazwa aplikacji WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="c3480-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="c3480-121">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="c3480-121">-Namespace</span></span>
<span data-ttu-id="c3480-122">Nazwa przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="c3480-122">Namespace Name.</span></span>

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

### <span data-ttu-id="c3480-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3480-123">-ResourceGroupName</span></span>
<span data-ttu-id="c3480-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c3480-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="c3480-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="c3480-125">-UserMetadata</span></span>
<span data-ttu-id="c3480-126">Pobiera lub ustawia wartość usermetadata jest symbolem zastępczym do przechowywania danych ciągu zdefiniowanych przez użytkownika dla punktu końcowego WcfRelay, np. może być używana do przechowywania danych opisowych, takich jak lista zespołów i ich informacje kontaktowe, a także mogą być przechowywane ustawienia konfiguracji zdefiniowane przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c3480-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the WcfRelay endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="c3480-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c3480-127">-Confirm</span></span>
<span data-ttu-id="c3480-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c3480-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3480-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3480-129">-WhatIf</span></span>
<span data-ttu-id="c3480-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3480-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3480-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c3480-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3480-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3480-132">CommonParameters</span></span>
<span data-ttu-id="c3480-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3480-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3480-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3480-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3480-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3480-135">INPUTS</span></span>

### <span data-ttu-id="c3480-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c3480-136">System.String</span></span>

### <span data-ttu-id="c3480-137">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="c3480-137">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="c3480-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3480-138">OUTPUTS</span></span>

### <span data-ttu-id="c3480-139">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="c3480-139">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="c3480-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c3480-140">NOTES</span></span>

## <span data-ttu-id="c3480-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3480-141">RELATED LINKS</span></span>
