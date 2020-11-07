---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
ms.openlocfilehash: f523f0d1166a40e04ac85344c0fc96640a140bb6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93886486"
---
# <span data-ttu-id="6be7e-101">Remove-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="6be7e-101">Remove-AzWcfRelay</span></span>

## <span data-ttu-id="6be7e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6be7e-102">SYNOPSIS</span></span>
<span data-ttu-id="6be7e-103">Usuwa WcfRelay z określonego obszaru nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="6be7e-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="6be7e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6be7e-104">SYNTAX</span></span>

```
Remove-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6be7e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6be7e-105">DESCRIPTION</span></span>
<span data-ttu-id="6be7e-106">Polecenie cmdlet **Remove-AzWcfRelay** usuwa WcfRelay z określonego obszaru nazw Relay.</span><span class="sxs-lookup"><span data-stu-id="6be7e-106">The **Remove-AzWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="6be7e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6be7e-107">EXAMPLES</span></span>

### <span data-ttu-id="6be7e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6be7e-108">Example 1</span></span>
```
PS C:\> Remove-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="6be7e-109">Usuwa WcfRelay `TestWCFRelay1` z obszaru nazw `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="6be7e-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="6be7e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6be7e-110">PARAMETERS</span></span>

### <span data-ttu-id="6be7e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6be7e-111">-DefaultProfile</span></span>
<span data-ttu-id="6be7e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6be7e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6be7e-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6be7e-113">-Name</span></span>
<span data-ttu-id="6be7e-114">Nazwa WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="6be7e-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="6be7e-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6be7e-115">-Namespace</span></span>
<span data-ttu-id="6be7e-116">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="6be7e-116">Namespace Name.</span></span>

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

### <span data-ttu-id="6be7e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6be7e-117">-ResourceGroupName</span></span>
<span data-ttu-id="6be7e-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6be7e-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="6be7e-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6be7e-119">-Confirm</span></span>
<span data-ttu-id="6be7e-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6be7e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6be7e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6be7e-121">-WhatIf</span></span>
<span data-ttu-id="6be7e-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6be7e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6be7e-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6be7e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6be7e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6be7e-124">CommonParameters</span></span>
<span data-ttu-id="6be7e-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6be7e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6be7e-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6be7e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6be7e-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6be7e-127">INPUTS</span></span>

### <span data-ttu-id="6be7e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6be7e-128">System.String</span></span>

## <span data-ttu-id="6be7e-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6be7e-129">OUTPUTS</span></span>

### <span data-ttu-id="6be7e-130">System. void</span><span class="sxs-lookup"><span data-stu-id="6be7e-130">System.Void</span></span>

## <span data-ttu-id="6be7e-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6be7e-131">NOTES</span></span>

## <span data-ttu-id="6be7e-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6be7e-132">RELATED LINKS</span></span>
