---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
ms.openlocfilehash: d0ac732a0feaffa187ec33d60f9587a7a6a1cff1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552372"
---
# <span data-ttu-id="6a814-101">Remove-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="6a814-101">Remove-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="6a814-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6a814-102">SYNOPSIS</span></span>
<span data-ttu-id="6a814-103">Usuwa obszar nazw z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6a814-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a814-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6a814-104">SYNTAX</span></span>

```
Remove-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a814-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6a814-105">DESCRIPTION</span></span>
<span data-ttu-id="6a814-106">Polecenie cmdlet **Remove-AzureRmRelayNamespace** usuwa obszar nazw z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6a814-106">The **Remove-AzureRmRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="6a814-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6a814-107">EXAMPLES</span></span>

### <span data-ttu-id="6a814-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6a814-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="6a814-109">Usuwa obszar nazw przekaźnika `TestNameSpace-Relay1` z określonej grupy zasobów `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="6a814-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="6a814-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6a814-110">PARAMETERS</span></span>

### <span data-ttu-id="6a814-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6a814-111">-Name</span></span>
<span data-ttu-id="6a814-112">Nazwa obszaru nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="6a814-112">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="6a814-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a814-113">-ResourceGroupName</span></span>
<span data-ttu-id="6a814-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6a814-114">Resource Group Name.</span></span>

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

### <span data-ttu-id="6a814-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6a814-115">-Confirm</span></span>
<span data-ttu-id="6a814-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a814-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a814-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a814-117">-WhatIf</span></span>
<span data-ttu-id="6a814-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a814-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a814-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6a814-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a814-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a814-120">-DefaultProfile</span></span>
<span data-ttu-id="6a814-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a814-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a814-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a814-122">CommonParameters</span></span>
<span data-ttu-id="6a814-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a814-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a814-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a814-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a814-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a814-125">INPUTS</span></span>

### <span data-ttu-id="6a814-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a814-126">-ResourceGroupName</span></span>
 <span data-ttu-id="6a814-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6a814-127">System.String</span></span>

### <span data-ttu-id="6a814-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6a814-128">-Name</span></span>
 <span data-ttu-id="6a814-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6a814-129">System.String</span></span>

## <span data-ttu-id="6a814-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6a814-130">OUTPUTS</span></span>

### <span data-ttu-id="6a814-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="6a814-131">System.Object</span></span>

## <span data-ttu-id="6a814-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6a814-132">NOTES</span></span>

## <span data-ttu-id="6a814-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a814-133">RELATED LINKS</span></span>

