---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 5d58fe0b998f7998da7b3a456d005570929cb848
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717307"
---
# <span data-ttu-id="2bfdc-101">Remove-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="2bfdc-101">Remove-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="2bfdc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2bfdc-102">SYNOPSIS</span></span>
<span data-ttu-id="2bfdc-103">Usuwa obszar nazw z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2bfdc-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bfdc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2bfdc-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bfdc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2bfdc-105">DESCRIPTION</span></span>
<span data-ttu-id="2bfdc-106">Polecenie cmdlet **Remove-AzureRmServiceBusNamespace** usuwa obszar nazw z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2bfdc-106">The **Remove-AzureRmServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="2bfdc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2bfdc-107">EXAMPLES</span></span>

### <span data-ttu-id="2bfdc-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2bfdc-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="2bfdc-109">Usuwa obszar nazw usługi Service Bus `SB-Example1` z określonej grupy zasobów `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="2bfdc-109">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="2bfdc-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2bfdc-110">PARAMETERS</span></span>

### <span data-ttu-id="2bfdc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bfdc-111">-DefaultProfile</span></span>
<span data-ttu-id="2bfdc-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2bfdc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bfdc-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2bfdc-113">-Name</span></span>
<span data-ttu-id="2bfdc-114">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="2bfdc-114">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bfdc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bfdc-115">-ResourceGroupName</span></span>
<span data-ttu-id="2bfdc-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="2bfdc-116">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bfdc-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2bfdc-117">-Confirm</span></span>
<span data-ttu-id="2bfdc-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bfdc-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bfdc-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bfdc-119">-WhatIf</span></span>
<span data-ttu-id="2bfdc-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bfdc-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bfdc-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2bfdc-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bfdc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bfdc-122">CommonParameters</span></span>
<span data-ttu-id="2bfdc-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bfdc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bfdc-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bfdc-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bfdc-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2bfdc-125">INPUTS</span></span>

### <span data-ttu-id="2bfdc-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="2bfdc-126">-ResourceGroup</span></span>
 <span data-ttu-id="2bfdc-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2bfdc-127">System.String</span></span>

### <span data-ttu-id="2bfdc-128">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="2bfdc-128">-NamespaceName</span></span>
 <span data-ttu-id="2bfdc-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2bfdc-129">System.String</span></span>

## <span data-ttu-id="2bfdc-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2bfdc-130">OUTPUTS</span></span>

### <span data-ttu-id="2bfdc-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="2bfdc-131">System.Object</span></span>

## <span data-ttu-id="2bfdc-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2bfdc-132">NOTES</span></span>

## <span data-ttu-id="2bfdc-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2bfdc-133">RELATED LINKS</span></span>

