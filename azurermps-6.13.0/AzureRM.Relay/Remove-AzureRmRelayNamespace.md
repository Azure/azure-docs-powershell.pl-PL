---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
ms.openlocfilehash: ac6327176c587bcb221a5ebddbb12ae9adeffbf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718781"
---
# <span data-ttu-id="540df-101">Remove-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="540df-101">Remove-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="540df-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="540df-102">SYNOPSIS</span></span>
<span data-ttu-id="540df-103">Usuwa obszar nazw z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="540df-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="540df-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="540df-104">SYNTAX</span></span>

```
Remove-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="540df-105">Opis</span><span class="sxs-lookup"><span data-stu-id="540df-105">DESCRIPTION</span></span>
<span data-ttu-id="540df-106">Polecenie cmdlet **Remove-AzureRmRelayNamespace** usuwa obszar nazw z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="540df-106">The **Remove-AzureRmRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="540df-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="540df-107">EXAMPLES</span></span>

### <span data-ttu-id="540df-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="540df-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="540df-109">Usuwa obszar nazw przekaźnika `TestNameSpace-Relay1` z określonej grupy zasobów `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="540df-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="540df-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="540df-110">PARAMETERS</span></span>

### <span data-ttu-id="540df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="540df-111">-DefaultProfile</span></span>
<span data-ttu-id="540df-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="540df-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="540df-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="540df-113">-Name</span></span>
<span data-ttu-id="540df-114">Nazwa obszaru nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="540df-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="540df-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="540df-115">-ResourceGroupName</span></span>
<span data-ttu-id="540df-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="540df-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="540df-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="540df-117">-Confirm</span></span>
<span data-ttu-id="540df-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="540df-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="540df-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="540df-119">-WhatIf</span></span>
<span data-ttu-id="540df-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="540df-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="540df-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="540df-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="540df-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="540df-122">CommonParameters</span></span>
<span data-ttu-id="540df-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="540df-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="540df-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="540df-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="540df-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="540df-125">INPUTS</span></span>

### <span data-ttu-id="540df-126">System. String</span><span class="sxs-lookup"><span data-stu-id="540df-126">System.String</span></span>


## <span data-ttu-id="540df-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="540df-127">OUTPUTS</span></span>

### <span data-ttu-id="540df-128">System. void</span><span class="sxs-lookup"><span data-stu-id="540df-128">System.Void</span></span>


## <span data-ttu-id="540df-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="540df-129">NOTES</span></span>

## <span data-ttu-id="540df-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="540df-130">RELATED LINKS</span></span>
