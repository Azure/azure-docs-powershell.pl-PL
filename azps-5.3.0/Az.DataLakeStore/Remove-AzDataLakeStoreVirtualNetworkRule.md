---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 9e455b7160b731f20e5dad6230b2015f73ca5390
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489086"
---
# <span data-ttu-id="9461d-101">Remove-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9461d-101">Remove-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="9461d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9461d-102">SYNOPSIS</span></span>
<span data-ttu-id="9461d-103">Usuwa określoną regułę sieci wirtualnej w określonym sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9461d-103">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="9461d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9461d-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreVirtualNetworkRule [-Account] <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9461d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9461d-105">DESCRIPTION</span></span>
<span data-ttu-id="9461d-106">Polecenie cmdlet **Remove-AzDataLakeStoreVirtualNetworkRule** usuwa określoną regułę sieci wirtualnej w określonym sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9461d-106">The **Remove-AzDataLakeStoreVirtualNetworkRule** cmdlet removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="9461d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9461d-107">EXAMPLES</span></span>

### <span data-ttu-id="9461d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9461d-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"
```

<span data-ttu-id="9461d-109">Usuwa regułę sieci wirtualnej "myVNET" z konta "DLS".</span><span class="sxs-lookup"><span data-stu-id="9461d-109">Removes virtual network rule "myVNET" from account "dls"</span></span>

## <span data-ttu-id="9461d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9461d-110">PARAMETERS</span></span>

### <span data-ttu-id="9461d-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="9461d-111">-Account</span></span>
<span data-ttu-id="9461d-112">Konto usługi Data Lake Store do aktualizowania reguły sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="9461d-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="9461d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9461d-113">-DefaultProfile</span></span>
<span data-ttu-id="9461d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9461d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9461d-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9461d-115">-Name</span></span>
<span data-ttu-id="9461d-116">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9461d-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="9461d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9461d-117">-PassThru</span></span>
<span data-ttu-id="9461d-118">Wskazuje, że należy zwrócić odpowiedź logiczną wskazującą wynik operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="9461d-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="9461d-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9461d-119">-Confirm</span></span>
<span data-ttu-id="9461d-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9461d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9461d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9461d-121">-WhatIf</span></span>
<span data-ttu-id="9461d-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9461d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9461d-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9461d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9461d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9461d-124">CommonParameters</span></span>
<span data-ttu-id="9461d-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9461d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9461d-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9461d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9461d-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9461d-127">INPUTS</span></span>

### <span data-ttu-id="9461d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9461d-128">System.String</span></span>

## <span data-ttu-id="9461d-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9461d-129">OUTPUTS</span></span>

### <span data-ttu-id="9461d-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9461d-130">System.Boolean</span></span>

## <span data-ttu-id="9461d-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9461d-131">NOTES</span></span>

## <span data-ttu-id="9461d-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9461d-132">RELATED LINKS</span></span>
