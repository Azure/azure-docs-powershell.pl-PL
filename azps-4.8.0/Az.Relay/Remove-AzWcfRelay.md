---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
ms.openlocfilehash: 238c4ecf92cbdd1dc6e9e0a430ec8e6ad200b967
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063246"
---
# <span data-ttu-id="71033-101">Remove-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="71033-101">Remove-AzWcfRelay</span></span>

## <span data-ttu-id="71033-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="71033-102">SYNOPSIS</span></span>
<span data-ttu-id="71033-103">Usuwa WcfRelay z określonego obszaru nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="71033-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="71033-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="71033-104">SYNTAX</span></span>

```
Remove-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71033-105">Opis</span><span class="sxs-lookup"><span data-stu-id="71033-105">DESCRIPTION</span></span>
<span data-ttu-id="71033-106">Polecenie cmdlet **Remove-AzWcfRelay** usuwa WcfRelay z określonego obszaru nazw Relay.</span><span class="sxs-lookup"><span data-stu-id="71033-106">The **Remove-AzWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="71033-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="71033-107">EXAMPLES</span></span>

### <span data-ttu-id="71033-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="71033-108">Example 1</span></span>
```
PS C:\> Remove-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="71033-109">Usuwa WcfRelay `TestWCFRelay1` z obszaru nazw `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="71033-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="71033-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="71033-110">PARAMETERS</span></span>

### <span data-ttu-id="71033-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71033-111">-DefaultProfile</span></span>
<span data-ttu-id="71033-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="71033-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71033-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="71033-113">-Name</span></span>
<span data-ttu-id="71033-114">Nazwa WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="71033-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="71033-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="71033-115">-Namespace</span></span>
<span data-ttu-id="71033-116">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="71033-116">Namespace Name.</span></span>

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

### <span data-ttu-id="71033-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71033-117">-ResourceGroupName</span></span>
<span data-ttu-id="71033-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="71033-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="71033-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="71033-119">-Confirm</span></span>
<span data-ttu-id="71033-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71033-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71033-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71033-121">-WhatIf</span></span>
<span data-ttu-id="71033-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71033-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71033-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="71033-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71033-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71033-124">CommonParameters</span></span>
<span data-ttu-id="71033-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71033-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71033-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71033-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71033-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71033-127">INPUTS</span></span>

### <span data-ttu-id="71033-128">System. String</span><span class="sxs-lookup"><span data-stu-id="71033-128">System.String</span></span>

## <span data-ttu-id="71033-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="71033-129">OUTPUTS</span></span>

### <span data-ttu-id="71033-130">System. void</span><span class="sxs-lookup"><span data-stu-id="71033-130">System.Void</span></span>

## <span data-ttu-id="71033-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="71033-131">NOTES</span></span>

## <span data-ttu-id="71033-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71033-132">RELATED LINKS</span></span>
