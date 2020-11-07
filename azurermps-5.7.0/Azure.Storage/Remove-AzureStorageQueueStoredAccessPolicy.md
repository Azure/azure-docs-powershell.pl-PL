---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 5bfdca4637f4d1504d8dbf18a923f8c1f0c082bd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719491"
---
# <span data-ttu-id="6ac60-101">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6ac60-101">Remove-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="6ac60-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ac60-102">SYNOPSIS</span></span>
<span data-ttu-id="6ac60-103">Usuwa zapisane zasady dostępu z kolejki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="6ac60-103">Removes a stored access policy from an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ac60-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ac60-104">SYNTAX</span></span>

```
Remove-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ac60-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6ac60-105">DESCRIPTION</span></span>
<span data-ttu-id="6ac60-106">Polecenie cmdlet **Remove-AzureStorageQueueStoredAccessPolicy** usuwa zapisane zasady dostępu z kolejki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="6ac60-106">The **Remove-AzureStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="6ac60-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ac60-107">EXAMPLES</span></span>

### <span data-ttu-id="6ac60-108">Przykład 1: usuwanie zapisanych zasad dostępu z kolejki magazynu</span><span class="sxs-lookup"><span data-stu-id="6ac60-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="6ac60-109">To polecenie usuwa zasady dostępu o nazwie Policy04 z kolejki magazynu o nazwie Moja kolejka.</span><span class="sxs-lookup"><span data-stu-id="6ac60-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="6ac60-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ac60-110">PARAMETERS</span></span>

### <span data-ttu-id="6ac60-111">-Context</span><span class="sxs-lookup"><span data-stu-id="6ac60-111">-Context</span></span>
<span data-ttu-id="6ac60-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="6ac60-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6ac60-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="6ac60-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6ac60-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ac60-114">-PassThru</span></span>
<span data-ttu-id="6ac60-115">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="6ac60-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="6ac60-116">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="6ac60-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="6ac60-117">-Policy</span><span class="sxs-lookup"><span data-stu-id="6ac60-117">-Policy</span></span>
<span data-ttu-id="6ac60-118">Określa nazwę zasad dostępu przechowywanych, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ac60-118">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6ac60-119">-Queue</span><span class="sxs-lookup"><span data-stu-id="6ac60-119">-Queue</span></span>
<span data-ttu-id="6ac60-120">Określa nazwę kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6ac60-120">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="6ac60-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6ac60-121">-Confirm</span></span>
<span data-ttu-id="6ac60-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ac60-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ac60-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ac60-123">-WhatIf</span></span>
<span data-ttu-id="6ac60-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ac60-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ac60-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6ac60-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ac60-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ac60-126">CommonParameters</span></span>
<span data-ttu-id="6ac60-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ac60-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ac60-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ac60-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ac60-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ac60-129">INPUTS</span></span>

### <span data-ttu-id="6ac60-130">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6ac60-130">IStorageContext</span></span>

<span data-ttu-id="6ac60-131">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="6ac60-131">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="6ac60-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ac60-132">OUTPUTS</span></span>

### <span data-ttu-id="6ac60-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6ac60-133">System.Boolean</span></span>

## <span data-ttu-id="6ac60-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ac60-134">NOTES</span></span>

## <span data-ttu-id="6ac60-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ac60-135">RELATED LINKS</span></span>

[<span data-ttu-id="6ac60-136">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6ac60-136">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="6ac60-137">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="6ac60-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="6ac60-138">Nowe — AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6ac60-138">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="6ac60-139">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6ac60-139">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)
