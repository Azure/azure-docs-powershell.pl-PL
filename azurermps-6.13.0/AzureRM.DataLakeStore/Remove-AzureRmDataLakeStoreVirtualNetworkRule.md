---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 196d0eba5119ab984f9ffc632a301d3e65157f63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717426"
---
# <span data-ttu-id="aa562-101">Remove-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="aa562-101">Remove-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="aa562-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa562-102">SYNOPSIS</span></span>
<span data-ttu-id="aa562-103">Usuwa określoną regułę sieci wirtualnej w określonym sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="aa562-103">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa562-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa562-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa562-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aa562-105">DESCRIPTION</span></span>
<span data-ttu-id="aa562-106">Polecenie cmdlet **Remove-AzureRmDataLakeStoreVirtualNetworkRule** usuwa określoną regułę sieci wirtualnej w określonym sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="aa562-106">The **Remove-AzureRmDataLakeStoreVirtualNetworkRule** cmdlet removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="aa562-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa562-107">EXAMPLES</span></span>

### <span data-ttu-id="aa562-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="aa562-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"
```

<span data-ttu-id="aa562-109">Usuwa regułę sieci wirtualnej "myVNET" z konta "DLS".</span><span class="sxs-lookup"><span data-stu-id="aa562-109">Removes virtual network rule "myVNET" from account "dls"</span></span>

## <span data-ttu-id="aa562-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa562-110">PARAMETERS</span></span>

### <span data-ttu-id="aa562-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="aa562-111">-Account</span></span>
<span data-ttu-id="aa562-112">Konto usługi Data Lake Store do aktualizowania reguły sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="aa562-112">The Data Lake Store account to update the virtual network rule in</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa562-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa562-113">-DefaultProfile</span></span>
<span data-ttu-id="aa562-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa562-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa562-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aa562-115">-Name</span></span>
<span data-ttu-id="aa562-116">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="aa562-116">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa562-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa562-117">-PassThru</span></span>
<span data-ttu-id="aa562-118">Wskazuje, że należy zwrócić odpowiedź logiczną wskazującą wynik operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="aa562-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa562-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aa562-119">-Confirm</span></span>
<span data-ttu-id="aa562-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa562-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa562-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa562-121">-WhatIf</span></span>
<span data-ttu-id="aa562-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa562-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa562-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="aa562-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa562-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa562-124">CommonParameters</span></span>
<span data-ttu-id="aa562-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa562-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa562-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa562-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa562-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa562-127">INPUTS</span></span>

### <span data-ttu-id="aa562-128">System. String</span><span class="sxs-lookup"><span data-stu-id="aa562-128">System.String</span></span>

### <span data-ttu-id="aa562-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="aa562-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="aa562-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa562-130">OUTPUTS</span></span>

### <span data-ttu-id="aa562-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aa562-131">System.Boolean</span></span>

## <span data-ttu-id="aa562-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa562-132">NOTES</span></span>

## <span data-ttu-id="aa562-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa562-133">RELATED LINKS</span></span>
