---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
ms.openlocfilehash: ae67aac391f2cce2a37be8a5a15a0fd0ea37cdd9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239239"
---
# <span data-ttu-id="01184-101">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="01184-101">Remove-AzBatchAccount</span></span>

## <span data-ttu-id="01184-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01184-102">SYNOPSIS</span></span>
<span data-ttu-id="01184-103">Usuwa konto usługi Batch.</span><span class="sxs-lookup"><span data-stu-id="01184-103">Removes a Batch account.</span></span>

## <span data-ttu-id="01184-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="01184-104">SYNTAX</span></span>

```
Remove-AzBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01184-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="01184-105">DESCRIPTION</span></span>
<span data-ttu-id="01184-106">Polecenie **cmdlet Remove-AzBatchAccount** usuwa konto usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="01184-106">The **Remove-AzBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="01184-107">To polecenie cmdlet wyświetli monit przed usunięciem konta, chyba że określisz parametr *Force.*</span><span class="sxs-lookup"><span data-stu-id="01184-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="01184-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="01184-108">EXAMPLES</span></span>

### <span data-ttu-id="01184-109">Przykład 1. Usuwanie konta wsadowego</span><span class="sxs-lookup"><span data-stu-id="01184-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="01184-110">To polecenie usuwa konto batch o nazwie Pfuller.</span><span class="sxs-lookup"><span data-stu-id="01184-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="01184-111">To polecenie wyświetla monit o potwierdzenie przed usunięciem konta.</span><span class="sxs-lookup"><span data-stu-id="01184-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="01184-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01184-112">PARAMETERS</span></span>

### <span data-ttu-id="01184-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="01184-113">-AccountName</span></span>
<span data-ttu-id="01184-114">Określa nazwę konta usługi Batch, które usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01184-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="01184-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01184-115">-DefaultProfile</span></span>
<span data-ttu-id="01184-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="01184-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01184-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="01184-117">-Force</span></span>
<span data-ttu-id="01184-118">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="01184-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="01184-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01184-119">-ResourceGroupName</span></span>
<span data-ttu-id="01184-120">Określa grupę zasobów dla konta, które to polecenie cmdlet usunie.</span><span class="sxs-lookup"><span data-stu-id="01184-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="01184-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="01184-121">-Confirm</span></span>
<span data-ttu-id="01184-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="01184-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01184-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01184-123">-WhatIf</span></span>
<span data-ttu-id="01184-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01184-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01184-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="01184-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01184-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01184-126">CommonParameters</span></span>
<span data-ttu-id="01184-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01184-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01184-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01184-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01184-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01184-129">INPUTS</span></span>

### <span data-ttu-id="01184-130">System.String</span><span class="sxs-lookup"><span data-stu-id="01184-130">System.String</span></span>

## <span data-ttu-id="01184-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01184-131">OUTPUTS</span></span>

### <span data-ttu-id="01184-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="01184-132">System.Void</span></span>

## <span data-ttu-id="01184-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="01184-133">NOTES</span></span>

## <span data-ttu-id="01184-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01184-134">RELATED LINKS</span></span>

[<span data-ttu-id="01184-135">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="01184-135">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="01184-136">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="01184-136">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="01184-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="01184-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="01184-138">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="01184-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
