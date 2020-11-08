---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
ms.openlocfilehash: ae67aac391f2cce2a37be8a5a15a0fd0ea37cdd9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221564"
---
# <span data-ttu-id="58968-101">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="58968-101">Remove-AzBatchAccount</span></span>

## <span data-ttu-id="58968-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58968-102">SYNOPSIS</span></span>
<span data-ttu-id="58968-103">Umożliwia usunięcie konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="58968-103">Removes a Batch account.</span></span>

## <span data-ttu-id="58968-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58968-104">SYNTAX</span></span>

```
Remove-AzBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58968-105">Opis</span><span class="sxs-lookup"><span data-stu-id="58968-105">DESCRIPTION</span></span>
<span data-ttu-id="58968-106">Polecenie cmdlet **Remove-AzBatchAccount** usuwa konto usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="58968-106">The **Remove-AzBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="58968-107">To polecenie cmdlet wyświetla monit przed usunięciem konta, chyba że zostanie określony parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="58968-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="58968-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58968-108">EXAMPLES</span></span>

### <span data-ttu-id="58968-109">Przykład 1. Usuń konto wsadowe</span><span class="sxs-lookup"><span data-stu-id="58968-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="58968-110">To polecenie usuwa konto wsadowe o nazwie pfuller.</span><span class="sxs-lookup"><span data-stu-id="58968-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="58968-111">To polecenie monituje o potwierdzenie przed usunięciem konta.</span><span class="sxs-lookup"><span data-stu-id="58968-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="58968-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58968-112">PARAMETERS</span></span>

### <span data-ttu-id="58968-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="58968-113">-AccountName</span></span>
<span data-ttu-id="58968-114">Określa nazwę konta wsadowego, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58968-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="58968-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58968-115">-DefaultProfile</span></span>
<span data-ttu-id="58968-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="58968-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58968-117">-Force</span><span class="sxs-lookup"><span data-stu-id="58968-117">-Force</span></span>
<span data-ttu-id="58968-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="58968-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="58968-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58968-119">-ResourceGroupName</span></span>
<span data-ttu-id="58968-120">Określa grupę zasobów konta, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58968-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="58968-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="58968-121">-Confirm</span></span>
<span data-ttu-id="58968-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58968-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58968-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58968-123">-WhatIf</span></span>
<span data-ttu-id="58968-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58968-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58968-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="58968-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58968-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58968-126">CommonParameters</span></span>
<span data-ttu-id="58968-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58968-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58968-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58968-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58968-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58968-129">INPUTS</span></span>

### <span data-ttu-id="58968-130">System. String</span><span class="sxs-lookup"><span data-stu-id="58968-130">System.String</span></span>

## <span data-ttu-id="58968-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58968-131">OUTPUTS</span></span>

### <span data-ttu-id="58968-132">System. void</span><span class="sxs-lookup"><span data-stu-id="58968-132">System.Void</span></span>

## <span data-ttu-id="58968-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58968-133">NOTES</span></span>

## <span data-ttu-id="58968-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58968-134">RELATED LINKS</span></span>

[<span data-ttu-id="58968-135">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="58968-135">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="58968-136">Nowe — AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="58968-136">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="58968-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="58968-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="58968-138">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="58968-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
