---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchAccount.md
ms.openlocfilehash: 3e460cddb83eacc1a012aebd009cd087ba1b68d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553039"
---
# <span data-ttu-id="79ae6-101">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="79ae6-101">Remove-AzureRmBatchAccount</span></span>

## <span data-ttu-id="79ae6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="79ae6-102">SYNOPSIS</span></span>
<span data-ttu-id="79ae6-103">Umożliwia usunięcie konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="79ae6-103">Removes a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79ae6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="79ae6-104">SYNTAX</span></span>

```
Remove-AzureRmBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79ae6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="79ae6-105">DESCRIPTION</span></span>
<span data-ttu-id="79ae6-106">Polecenie cmdlet **Remove-AzureRmBatchAccount** usuwa konto usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="79ae6-106">The **Remove-AzureRmBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="79ae6-107">To polecenie cmdlet wyświetla monit przed usunięciem konta, chyba że zostanie określony parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="79ae6-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="79ae6-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="79ae6-108">EXAMPLES</span></span>

### <span data-ttu-id="79ae6-109">Przykład 1. Usuń konto wsadowe</span><span class="sxs-lookup"><span data-stu-id="79ae6-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="79ae6-110">To polecenie usuwa konto wsadowe o nazwie pfuller.</span><span class="sxs-lookup"><span data-stu-id="79ae6-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="79ae6-111">To polecenie monituje o potwierdzenie przed usunięciem konta.</span><span class="sxs-lookup"><span data-stu-id="79ae6-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="79ae6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="79ae6-112">PARAMETERS</span></span>

### <span data-ttu-id="79ae6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="79ae6-113">-AccountName</span></span>
<span data-ttu-id="79ae6-114">Określa nazwę konta wsadowego, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79ae6-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79ae6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79ae6-115">-DefaultProfile</span></span>
<span data-ttu-id="79ae6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="79ae6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79ae6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="79ae6-117">-Force</span></span>
<span data-ttu-id="79ae6-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="79ae6-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79ae6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79ae6-119">-ResourceGroupName</span></span>
<span data-ttu-id="79ae6-120">Określa grupę zasobów konta, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79ae6-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79ae6-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79ae6-121">-Confirm</span></span>
<span data-ttu-id="79ae6-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79ae6-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79ae6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79ae6-123">-WhatIf</span></span>
<span data-ttu-id="79ae6-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79ae6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79ae6-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="79ae6-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79ae6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79ae6-126">CommonParameters</span></span>
<span data-ttu-id="79ae6-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79ae6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79ae6-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79ae6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79ae6-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79ae6-129">INPUTS</span></span>

### <span data-ttu-id="79ae6-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="79ae6-130">None</span></span>
<span data-ttu-id="79ae6-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="79ae6-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="79ae6-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="79ae6-132">OUTPUTS</span></span>

## <span data-ttu-id="79ae6-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="79ae6-133">NOTES</span></span>

## <span data-ttu-id="79ae6-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79ae6-134">RELATED LINKS</span></span>

[<span data-ttu-id="79ae6-135">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="79ae6-135">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="79ae6-136">Nowe — AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="79ae6-136">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="79ae6-137">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="79ae6-137">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="79ae6-138">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="79ae6-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


