---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayHybridConnection.md
ms.openlocfilehash: a78d4091fad7738cdf769eb402aacc508e5f137d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708453"
---
# <span data-ttu-id="837f8-101">Set-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="837f8-101">Set-AzRelayHybridConnection</span></span>

## <span data-ttu-id="837f8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="837f8-102">SYNOPSIS</span></span>
<span data-ttu-id="837f8-103">Umożliwia zaktualizowanie opisu HybridConnection w określonej przestrzeni nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="837f8-103">Updates the description of a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="837f8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="837f8-104">SYNTAX</span></span>

### <span data-ttu-id="837f8-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="837f8-105">HybridConnectionInputObjectSet</span></span>
```
Set-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSHybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="837f8-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="837f8-106">HybridConnectionPropertiesSet</span></span>
```
Set-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="837f8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="837f8-107">DESCRIPTION</span></span>
<span data-ttu-id="837f8-108">Polecenie cmdlet Set-AzRelayHybridConnection aktualizuje opis HybridConnection w określonej przestrzeni nazw Relay.</span><span class="sxs-lookup"><span data-stu-id="837f8-108">The Set-AzRelayHybridConnection cmdlet updates the description for the HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="837f8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="837f8-109">EXAMPLES</span></span>

### <span data-ttu-id="837f8-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="837f8-110">Example 1</span></span>
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

### <span data-ttu-id="837f8-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="837f8-111">Example 2</span></span>
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

<span data-ttu-id="837f8-112">Umożliwia zaktualizowanie określonego HybridConnection przy użyciu nowego opisu w określonym obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="837f8-112">Updates the specified HybridConnection with a new description in the specified namespace.</span></span>
<span data-ttu-id="837f8-113">W tym przykładzie zostanie zaktualizowana właściwość UserMetadata o nową wartość.</span><span class="sxs-lookup"><span data-stu-id="837f8-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="837f8-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="837f8-114">PARAMETERS</span></span>

### <span data-ttu-id="837f8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="837f8-115">-DefaultProfile</span></span>
<span data-ttu-id="837f8-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="837f8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="837f8-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="837f8-117">-InputObject</span></span>
<span data-ttu-id="837f8-118">Obiekt HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="837f8-118">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="837f8-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="837f8-119">-Name</span></span>
<span data-ttu-id="837f8-120">Nazwa HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="837f8-120">HybridConnections Name.</span></span>

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

### <span data-ttu-id="837f8-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="837f8-121">-Namespace</span></span>
<span data-ttu-id="837f8-122">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="837f8-122">Namespace Name.</span></span>

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

### <span data-ttu-id="837f8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="837f8-123">-ResourceGroupName</span></span>
<span data-ttu-id="837f8-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="837f8-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="837f8-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="837f8-125">-UserMetadata</span></span>
<span data-ttu-id="837f8-126">Pobiera lub ustawia usermetadata jest symbolem zastępczym, aby można było przechowywać dane ciągu zdefiniowanego przez użytkownika dla punktu końcowego HybridConnection. na przykład można go użyć do przechowywania danych opisujących, takich jak lista zespołów i informacji kontaktowych, również w celu przechowywania ustawień konfiguracji zdefiniowanych przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="837f8-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="837f8-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="837f8-127">-Confirm</span></span>
<span data-ttu-id="837f8-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="837f8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="837f8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="837f8-129">-WhatIf</span></span>
<span data-ttu-id="837f8-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="837f8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="837f8-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="837f8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="837f8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="837f8-132">CommonParameters</span></span>
<span data-ttu-id="837f8-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="837f8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="837f8-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="837f8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="837f8-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="837f8-135">INPUTS</span></span>

### <span data-ttu-id="837f8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="837f8-136">System.String</span></span>

### <span data-ttu-id="837f8-137">Microsoft. Azure. Commands. Relay. modele. PSHybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="837f8-137">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttibutes</span></span>

## <span data-ttu-id="837f8-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="837f8-138">OUTPUTS</span></span>

### <span data-ttu-id="837f8-139">Microsoft. Azure. Commands. Relay. modele. PSHybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="837f8-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttibutes</span></span>

## <span data-ttu-id="837f8-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="837f8-140">NOTES</span></span>

## <span data-ttu-id="837f8-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="837f8-141">RELATED LINKS</span></span>
