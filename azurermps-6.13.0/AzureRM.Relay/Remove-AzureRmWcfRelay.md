---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
ms.openlocfilehash: 5e49497f8784e9686c84cb75dde4b8fd4297578d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543528"
---
# <span data-ttu-id="70d9a-101">Remove-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="70d9a-101">Remove-AzureRmWcfRelay</span></span>

## <span data-ttu-id="70d9a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="70d9a-102">SYNOPSIS</span></span>
<span data-ttu-id="70d9a-103">Usuwa WcfRelay z określonego obszaru nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="70d9a-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70d9a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="70d9a-104">SYNTAX</span></span>

```
Remove-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70d9a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="70d9a-105">DESCRIPTION</span></span>
<span data-ttu-id="70d9a-106">Polecenie cmdlet **Remove-AzureRmWcfRelay** usuwa WcfRelay z określonego obszaru nazw Relay.</span><span class="sxs-lookup"><span data-stu-id="70d9a-106">The **Remove-AzureRmWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="70d9a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="70d9a-107">EXAMPLES</span></span>

### <span data-ttu-id="70d9a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="70d9a-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="70d9a-109">Usuwa WcfRelay `TestWCFRelay1` z obszaru nazw `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="70d9a-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="70d9a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70d9a-110">PARAMETERS</span></span>

### <span data-ttu-id="70d9a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70d9a-111">-DefaultProfile</span></span>
<span data-ttu-id="70d9a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="70d9a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70d9a-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="70d9a-113">-Name</span></span>
<span data-ttu-id="70d9a-114">Nazwa WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="70d9a-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="70d9a-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="70d9a-115">-Namespace</span></span>
<span data-ttu-id="70d9a-116">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="70d9a-116">Namespace Name.</span></span>

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

### <span data-ttu-id="70d9a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70d9a-117">-ResourceGroupName</span></span>
<span data-ttu-id="70d9a-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="70d9a-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="70d9a-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="70d9a-119">-Confirm</span></span>
<span data-ttu-id="70d9a-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70d9a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70d9a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70d9a-121">-WhatIf</span></span>
<span data-ttu-id="70d9a-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70d9a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70d9a-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="70d9a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70d9a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70d9a-124">CommonParameters</span></span>
<span data-ttu-id="70d9a-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70d9a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="70d9a-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70d9a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70d9a-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70d9a-127">INPUTS</span></span>

### <span data-ttu-id="70d9a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="70d9a-128">System.String</span></span>


## <span data-ttu-id="70d9a-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="70d9a-129">OUTPUTS</span></span>

### <span data-ttu-id="70d9a-130">System. void</span><span class="sxs-lookup"><span data-stu-id="70d9a-130">System.Void</span></span>


## <span data-ttu-id="70d9a-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="70d9a-131">NOTES</span></span>

## <span data-ttu-id="70d9a-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70d9a-132">RELATED LINKS</span></span>
