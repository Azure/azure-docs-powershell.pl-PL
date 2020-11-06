---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueueStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 94c5bc28ae381227366b5461b51a2da7fd6feccd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547272"
---
# <span data-ttu-id="9ce7e-101">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9ce7e-101">Remove-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="9ce7e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9ce7e-102">SYNOPSIS</span></span>
<span data-ttu-id="9ce7e-103">Usuwa zapisane zasady dostępu z kolejki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-103">Removes a stored access policy from an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ce7e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9ce7e-104">SYNTAX</span></span>

```
Remove-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ce7e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9ce7e-105">DESCRIPTION</span></span>
<span data-ttu-id="9ce7e-106">Polecenie cmdlet **Remove-AzureStorageQueueStoredAccessPolicy** usuwa zapisane zasady dostępu z kolejki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-106">The **Remove-AzureStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="9ce7e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9ce7e-107">EXAMPLES</span></span>

### <span data-ttu-id="9ce7e-108">Przykład 1: usuwanie zapisanych zasad dostępu z kolejki magazynu</span><span class="sxs-lookup"><span data-stu-id="9ce7e-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="9ce7e-109">To polecenie usuwa zasady dostępu o nazwie Policy04 z kolejki magazynu o nazwie Moja kolejka.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="9ce7e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ce7e-110">PARAMETERS</span></span>

### <span data-ttu-id="9ce7e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="9ce7e-111">-Context</span></span>
<span data-ttu-id="9ce7e-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9ce7e-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ce7e-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ce7e-114">-PassThru</span></span>
<span data-ttu-id="9ce7e-115">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="9ce7e-116">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="9ce7e-117">-Policy</span><span class="sxs-lookup"><span data-stu-id="9ce7e-117">-Policy</span></span>
<span data-ttu-id="9ce7e-118">Określa nazwę zasad dostępu przechowywanych, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-118">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ce7e-119">-Queue</span><span class="sxs-lookup"><span data-stu-id="9ce7e-119">-Queue</span></span>
<span data-ttu-id="9ce7e-120">Określa nazwę kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-120">Specifies the Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ce7e-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9ce7e-121">-Confirm</span></span>
<span data-ttu-id="9ce7e-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ce7e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ce7e-123">-WhatIf</span></span>
<span data-ttu-id="9ce7e-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ce7e-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ce7e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ce7e-126">CommonParameters</span></span>
<span data-ttu-id="9ce7e-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ce7e-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ce7e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ce7e-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ce7e-129">INPUTS</span></span>

### <span data-ttu-id="9ce7e-130">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9ce7e-130">IStorageContext</span></span>

<span data-ttu-id="9ce7e-131">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="9ce7e-131">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="9ce7e-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9ce7e-132">OUTPUTS</span></span>

### <span data-ttu-id="9ce7e-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9ce7e-133">System.Boolean</span></span>

## <span data-ttu-id="9ce7e-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9ce7e-134">NOTES</span></span>

## <span data-ttu-id="9ce7e-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ce7e-135">RELATED LINKS</span></span>

[<span data-ttu-id="9ce7e-136">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9ce7e-136">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="9ce7e-137">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="9ce7e-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="9ce7e-138">Nowe — AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9ce7e-138">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="9ce7e-139">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9ce7e-139">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)
