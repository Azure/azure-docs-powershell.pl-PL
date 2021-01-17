---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
ms.openlocfilehash: ae67aac391f2cce2a37be8a5a15a0fd0ea37cdd9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361272"
---
# <span data-ttu-id="9dce1-101">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="9dce1-101">Remove-AzBatchAccount</span></span>

## <span data-ttu-id="9dce1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9dce1-102">SYNOPSIS</span></span>
<span data-ttu-id="9dce1-103">Umożliwia usunięcie konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="9dce1-103">Removes a Batch account.</span></span>

## <span data-ttu-id="9dce1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9dce1-104">SYNTAX</span></span>

```
Remove-AzBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dce1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9dce1-105">DESCRIPTION</span></span>
<span data-ttu-id="9dce1-106">Polecenie cmdlet **Remove-AzBatchAccount** usuwa konto usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="9dce1-106">The **Remove-AzBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="9dce1-107">To polecenie cmdlet wyświetla monit przed usunięciem konta, chyba że zostanie określony parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="9dce1-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="9dce1-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9dce1-108">EXAMPLES</span></span>

### <span data-ttu-id="9dce1-109">Przykład 1. Usuń konto wsadowe</span><span class="sxs-lookup"><span data-stu-id="9dce1-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="9dce1-110">To polecenie usuwa konto wsadowe o nazwie pfuller.</span><span class="sxs-lookup"><span data-stu-id="9dce1-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="9dce1-111">To polecenie monituje o potwierdzenie przed usunięciem konta.</span><span class="sxs-lookup"><span data-stu-id="9dce1-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="9dce1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9dce1-112">PARAMETERS</span></span>

### <span data-ttu-id="9dce1-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9dce1-113">-AccountName</span></span>
<span data-ttu-id="9dce1-114">Określa nazwę konta wsadowego, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9dce1-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dce1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dce1-115">-DefaultProfile</span></span>
<span data-ttu-id="9dce1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9dce1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9dce1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="9dce1-117">-Force</span></span>
<span data-ttu-id="9dce1-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9dce1-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9dce1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dce1-119">-ResourceGroupName</span></span>
<span data-ttu-id="9dce1-120">Określa grupę zasobów konta, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9dce1-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dce1-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9dce1-121">-Confirm</span></span>
<span data-ttu-id="9dce1-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9dce1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dce1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dce1-123">-WhatIf</span></span>
<span data-ttu-id="9dce1-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9dce1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dce1-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9dce1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dce1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dce1-126">CommonParameters</span></span>
<span data-ttu-id="9dce1-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dce1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dce1-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9dce1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dce1-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9dce1-129">INPUTS</span></span>

### <span data-ttu-id="9dce1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9dce1-130">System.String</span></span>

## <span data-ttu-id="9dce1-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9dce1-131">OUTPUTS</span></span>

### <span data-ttu-id="9dce1-132">System. void</span><span class="sxs-lookup"><span data-stu-id="9dce1-132">System.Void</span></span>

## <span data-ttu-id="9dce1-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9dce1-133">NOTES</span></span>

## <span data-ttu-id="9dce1-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9dce1-134">RELATED LINKS</span></span>

[<span data-ttu-id="9dce1-135">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="9dce1-135">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="9dce1-136">Nowe — AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="9dce1-136">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="9dce1-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="9dce1-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="9dce1-138">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="9dce1-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
