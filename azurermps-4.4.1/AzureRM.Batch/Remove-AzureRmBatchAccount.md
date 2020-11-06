---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchAccount.md
ms.openlocfilehash: 3de75d2c8e7ed69a8f5be02833dd002ee5fbf016
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549260"
---
# <span data-ttu-id="8a0d4-101">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="8a0d4-101">Remove-AzureRmBatchAccount</span></span>

## <span data-ttu-id="8a0d4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8a0d4-102">SYNOPSIS</span></span>
<span data-ttu-id="8a0d4-103">Umożliwia usunięcie konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="8a0d4-103">Removes a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a0d4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8a0d4-104">SYNTAX</span></span>

```
Remove-AzureRmBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a0d4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8a0d4-105">DESCRIPTION</span></span>
<span data-ttu-id="8a0d4-106">Polecenie cmdlet **Remove-AzureRmBatchAccount** usuwa konto usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="8a0d4-106">The **Remove-AzureRmBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="8a0d4-107">To polecenie cmdlet wyświetla monit przed usunięciem konta, chyba że zostanie określony parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="8a0d4-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="8a0d4-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8a0d4-108">EXAMPLES</span></span>

### <span data-ttu-id="8a0d4-109">Przykład 1. Usuń konto wsadowe</span><span class="sxs-lookup"><span data-stu-id="8a0d4-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="8a0d4-110">To polecenie usuwa konto wsadowe o nazwie pfuller.</span><span class="sxs-lookup"><span data-stu-id="8a0d4-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="8a0d4-111">To polecenie monituje o potwierdzenie przed usunięciem konta.</span><span class="sxs-lookup"><span data-stu-id="8a0d4-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="8a0d4-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8a0d4-112">PARAMETERS</span></span>

### <span data-ttu-id="8a0d4-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8a0d4-113">-AccountName</span></span>
<span data-ttu-id="8a0d4-114">Określa nazwę konta wsadowego, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a0d4-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8a0d4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8a0d4-115">-Force</span></span>
<span data-ttu-id="8a0d4-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8a0d4-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8a0d4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a0d4-117">-ResourceGroupName</span></span>
<span data-ttu-id="8a0d4-118">Określa grupę zasobów konta, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a0d4-118">Specifies the resource group of the account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8a0d4-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8a0d4-119">-Confirm</span></span>
<span data-ttu-id="8a0d4-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a0d4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a0d4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a0d4-121">-WhatIf</span></span>
<span data-ttu-id="8a0d4-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a0d4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a0d4-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8a0d4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a0d4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a0d4-124">-DefaultProfile</span></span>
<span data-ttu-id="8a0d4-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8a0d4-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a0d4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a0d4-126">CommonParameters</span></span>
<span data-ttu-id="8a0d4-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a0d4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a0d4-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a0d4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a0d4-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a0d4-129">INPUTS</span></span>

## <span data-ttu-id="8a0d4-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8a0d4-130">OUTPUTS</span></span>

## <span data-ttu-id="8a0d4-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8a0d4-131">NOTES</span></span>

## <span data-ttu-id="8a0d4-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a0d4-132">RELATED LINKS</span></span>

[<span data-ttu-id="8a0d4-133">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="8a0d4-133">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="8a0d4-134">Nowe — AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="8a0d4-134">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="8a0d4-135">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="8a0d4-135">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="8a0d4-136">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="8a0d4-136">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


