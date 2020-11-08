---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
ms.openlocfilehash: 463ef6d1d23ffe809d8810a9cbf4dd0ebf1ff578
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221666"
---
# <span data-ttu-id="4beca-101">Remove-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="4beca-101">Remove-AzRelayNamespace</span></span>

## <span data-ttu-id="4beca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4beca-102">SYNOPSIS</span></span>
<span data-ttu-id="4beca-103">Usuwa obszar nazw z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4beca-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="4beca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4beca-104">SYNTAX</span></span>

```
Remove-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4beca-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4beca-105">DESCRIPTION</span></span>
<span data-ttu-id="4beca-106">Polecenie cmdlet **Remove-AzRelayNamespace** usuwa obszar nazw z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4beca-106">The **Remove-AzRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="4beca-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4beca-107">EXAMPLES</span></span>

### <span data-ttu-id="4beca-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4beca-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="4beca-109">Usuwa obszar nazw przekaźnika `TestNameSpace-Relay1` z określonej grupy zasobów `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="4beca-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="4beca-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4beca-110">PARAMETERS</span></span>

### <span data-ttu-id="4beca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4beca-111">-DefaultProfile</span></span>
<span data-ttu-id="4beca-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4beca-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4beca-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4beca-113">-Name</span></span>
<span data-ttu-id="4beca-114">Nazwa obszaru nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="4beca-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="4beca-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4beca-115">-ResourceGroupName</span></span>
<span data-ttu-id="4beca-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4beca-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="4beca-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4beca-117">-Confirm</span></span>
<span data-ttu-id="4beca-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4beca-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4beca-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4beca-119">-WhatIf</span></span>
<span data-ttu-id="4beca-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4beca-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4beca-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4beca-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4beca-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4beca-122">CommonParameters</span></span>
<span data-ttu-id="4beca-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4beca-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4beca-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4beca-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4beca-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4beca-125">INPUTS</span></span>

### <span data-ttu-id="4beca-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4beca-126">System.String</span></span>

## <span data-ttu-id="4beca-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4beca-127">OUTPUTS</span></span>

### <span data-ttu-id="4beca-128">System. void</span><span class="sxs-lookup"><span data-stu-id="4beca-128">System.Void</span></span>

## <span data-ttu-id="4beca-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4beca-129">NOTES</span></span>

## <span data-ttu-id="4beca-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4beca-130">RELATED LINKS</span></span>
