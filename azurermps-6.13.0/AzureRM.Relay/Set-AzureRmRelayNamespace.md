---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
ms.openlocfilehash: 6bb333de426236099bed7402fc4756181415c4ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716762"
---
# <span data-ttu-id="660b7-101">Set-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="660b7-101">Set-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="660b7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="660b7-102">SYNOPSIS</span></span>
<span data-ttu-id="660b7-103">Umożliwia zaktualizowanie opisu istniejącego obszaru nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="660b7-103">Updates the description of an existing Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="660b7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="660b7-104">SYNTAX</span></span>

```
Set-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="660b7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="660b7-105">DESCRIPTION</span></span>
<span data-ttu-id="660b7-106">Polecenie cmdlet **Set-AzureRmRelayNamespace** umożliwia zaktualizowanie opisu określonego obszaru nazw przekaźnika w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="660b7-106">The **Set-AzureRmRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="660b7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="660b7-107">EXAMPLES</span></span>

### <span data-ttu-id="660b7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="660b7-108">Example 1</span></span>
```
PS C:\> Set-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

ProvisioningState  :
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           :
Location           :
Tags               : {[tag2, Tag2Value]}
Id                 :
Name               :
Type               :
```

<span data-ttu-id="660b7-109">Umożliwia zaktualizowanie obszaru nazw przekazywania przy użyciu nowego opisu.</span><span class="sxs-lookup"><span data-stu-id="660b7-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="660b7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="660b7-110">PARAMETERS</span></span>

### <span data-ttu-id="660b7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="660b7-111">-DefaultProfile</span></span>
<span data-ttu-id="660b7-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="660b7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="660b7-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="660b7-113">-InputObject</span></span>
<span data-ttu-id="660b7-114">Obiekt przekazujący obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="660b7-114">Relay Namespace object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="660b7-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="660b7-115">-Name</span></span>
<span data-ttu-id="660b7-116">Nazwa obszaru nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="660b7-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="660b7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="660b7-117">-ResourceGroupName</span></span>
<span data-ttu-id="660b7-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="660b7-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="660b7-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="660b7-119">-Tag</span></span>
<span data-ttu-id="660b7-120">Hashtable, które reprezentują znacznik zasobu.</span><span class="sxs-lookup"><span data-stu-id="660b7-120">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="660b7-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="660b7-121">-Confirm</span></span>
<span data-ttu-id="660b7-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="660b7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="660b7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="660b7-123">-WhatIf</span></span>
<span data-ttu-id="660b7-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="660b7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="660b7-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="660b7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="660b7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="660b7-126">CommonParameters</span></span>
<span data-ttu-id="660b7-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="660b7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="660b7-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="660b7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="660b7-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="660b7-129">INPUTS</span></span>

### <span data-ttu-id="660b7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="660b7-130">System.String</span></span>
<span data-ttu-id="660b7-131">System. Collections. Hashtable Microsoft. Azure. Commands. Relay. modele. RelayNamespaceAttirbutesUpdateParameter</span><span class="sxs-lookup"><span data-stu-id="660b7-131">System.Collections.Hashtable Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span></span>


## <span data-ttu-id="660b7-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="660b7-132">OUTPUTS</span></span>

### <span data-ttu-id="660b7-133">Microsoft. Azure. Commands. Relay. modele. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="660b7-133">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>


## <span data-ttu-id="660b7-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="660b7-134">NOTES</span></span>

## <span data-ttu-id="660b7-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="660b7-135">RELATED LINKS</span></span>
