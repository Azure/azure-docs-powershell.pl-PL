---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/set-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayHybridConnection.md
ms.openlocfilehash: 10fc65f492c76a3b240bd2287b080d56bb20836e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000410"
---
# <span data-ttu-id="fb87f-101">Set-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="fb87f-101">Set-AzRelayHybridConnection</span></span>

## <span data-ttu-id="fb87f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb87f-102">SYNOPSIS</span></span>
<span data-ttu-id="fb87f-103">Aktualizuje opis połączenia hybrydowego w określonej przestrzeni nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="fb87f-103">Updates the description of a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="fb87f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fb87f-104">SYNTAX</span></span>

### <span data-ttu-id="fb87f-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fb87f-105">HybridConnectionInputObjectSet</span></span>
```
Set-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSHybridConnectionAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb87f-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="fb87f-106">HybridConnectionPropertiesSet</span></span>
```
Set-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb87f-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="fb87f-107">DESCRIPTION</span></span>
<span data-ttu-id="fb87f-108">Polecenie Set-AzRelayHybridConnection aktualizuje opis połączenia hybrydowego w określonej przestrzeni nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="fb87f-108">The Set-AzRelayHybridConnection cmdlet updates the description for the HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="fb87f-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fb87f-109">EXAMPLES</span></span>

### <span data-ttu-id="fb87f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fb87f-110">Example 1</span></span>
```
PS C:\>
PS C:\> $GetHybrid = Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
PS C:\> $GetHybrid.UserMetadata = "Test UserMetadata"
PS C:\> Set-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -InputObject $GetHybrid

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:08:11 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : Test UserMetadata
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n2
Name                        : TestHybirdConnection2
Type                        : Microsoft.Relay/HybridConnections
```

### <span data-ttu-id="fb87f-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fb87f-111">Example 2</span></span>
```
PS C:\> Set-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -UserMetadata = "Test UserMetadata updated"

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:10:25 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : Test UserMetadata updated
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n1
Name                        : TestHybirdConnection1
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="fb87f-112">Aktualizuje określony program HybridConnection o nowy opis w określonej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="fb87f-112">Updates the specified HybridConnection with a new description in the specified namespace.</span></span>
<span data-ttu-id="fb87f-113">W tym przykładzie właściwość UserMetadata jest aktualizowana przy użyciu nowej wartości.</span><span class="sxs-lookup"><span data-stu-id="fb87f-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="fb87f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb87f-114">PARAMETERS</span></span>

### <span data-ttu-id="fb87f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb87f-115">-DefaultProfile</span></span>
<span data-ttu-id="fb87f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb87f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb87f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb87f-117">-InputObject</span></span>
<span data-ttu-id="fb87f-118">Obiekt HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="fb87f-118">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes
Parameter Sets: HybridConnectionInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb87f-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fb87f-119">-Name</span></span>
<span data-ttu-id="fb87f-120">Nazwa usługi HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="fb87f-120">HybridConnections Name.</span></span>

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

### <span data-ttu-id="fb87f-121">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="fb87f-121">-Namespace</span></span>
<span data-ttu-id="fb87f-122">Nazwa przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="fb87f-122">Namespace Name.</span></span>

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

### <span data-ttu-id="fb87f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb87f-123">-ResourceGroupName</span></span>
<span data-ttu-id="fb87f-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fb87f-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="fb87f-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="fb87f-125">-UserMetadata</span></span>
<span data-ttu-id="fb87f-126">Pobiera lub ustawia dane użytkownika jest symbolem zastępczym do przechowywania danych ciągu zdefiniowanych przez użytkownika dla punktu końcowego połączenia hybrydowego, np. może być używana do przechowywania danych opisowych, takich jak lista zespołów i ich informacje kontaktowe, a także mogą być przechowywane ustawienia konfiguracji zdefiniowane przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="fb87f-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb87f-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fb87f-127">-Confirm</span></span>
<span data-ttu-id="fb87f-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fb87f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb87f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb87f-129">-WhatIf</span></span>
<span data-ttu-id="fb87f-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb87f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb87f-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fb87f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb87f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb87f-132">CommonParameters</span></span>
<span data-ttu-id="fb87f-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb87f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb87f-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb87f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb87f-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb87f-135">INPUTS</span></span>

### <span data-ttu-id="fb87f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="fb87f-136">System.String</span></span>

### <span data-ttu-id="fb87f-137">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="fb87f-137">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="fb87f-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb87f-138">OUTPUTS</span></span>

### <span data-ttu-id="fb87f-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="fb87f-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="fb87f-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fb87f-140">NOTES</span></span>

## <span data-ttu-id="fb87f-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb87f-141">RELATED LINKS</span></span>
