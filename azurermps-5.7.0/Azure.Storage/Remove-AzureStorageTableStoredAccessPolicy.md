---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: a9e1290c5933d54481c57b051e170568653eee5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549055"
---
# <span data-ttu-id="421fd-101">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="421fd-101">Remove-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="421fd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="421fd-102">SYNOPSIS</span></span>
<span data-ttu-id="421fd-103">Usuwa zapisane zasady dostępu z tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="421fd-103">Removes a stored access policy from an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="421fd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="421fd-104">SYNTAX</span></span>

```
Remove-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="421fd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="421fd-105">DESCRIPTION</span></span>
<span data-ttu-id="421fd-106">Polecenie cmdlet **Remove-AzureStorageTableStoredAccessPolicy** usuwa zapisane zasady dostępu z tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="421fd-106">The **Remove-AzureStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="421fd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="421fd-107">EXAMPLES</span></span>

### <span data-ttu-id="421fd-108">Przykład 1: usuwanie zapisanych zasad dostępu z tabeli magazynu</span><span class="sxs-lookup"><span data-stu-id="421fd-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="421fd-109">To polecenie usuwa zasady o nazwie Policy05 z tabeli magazynu o nazwie MyTable.</span><span class="sxs-lookup"><span data-stu-id="421fd-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="421fd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="421fd-110">PARAMETERS</span></span>

### <span data-ttu-id="421fd-111">-Context</span><span class="sxs-lookup"><span data-stu-id="421fd-111">-Context</span></span>
<span data-ttu-id="421fd-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="421fd-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="421fd-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="421fd-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="421fd-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="421fd-114">-PassThru</span></span>
<span data-ttu-id="421fd-115">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="421fd-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="421fd-116">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="421fd-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="421fd-117">-Policy</span><span class="sxs-lookup"><span data-stu-id="421fd-117">-Policy</span></span>
<span data-ttu-id="421fd-118">Określa nazwę zasad dostępu przechowywanych, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="421fd-118">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="421fd-119">-Table</span><span class="sxs-lookup"><span data-stu-id="421fd-119">-Table</span></span>
<span data-ttu-id="421fd-120">Określa nazwę tabeli platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="421fd-120">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="421fd-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="421fd-121">-Confirm</span></span>
<span data-ttu-id="421fd-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="421fd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="421fd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="421fd-123">-WhatIf</span></span>
<span data-ttu-id="421fd-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="421fd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="421fd-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="421fd-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="421fd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="421fd-126">CommonParameters</span></span>
<span data-ttu-id="421fd-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="421fd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="421fd-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="421fd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="421fd-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="421fd-129">INPUTS</span></span>

### <span data-ttu-id="421fd-130">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="421fd-130">IStorageContext</span></span>

<span data-ttu-id="421fd-131">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="421fd-131">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="421fd-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="421fd-132">OUTPUTS</span></span>

### <span data-ttu-id="421fd-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="421fd-133">System.Boolean</span></span>

## <span data-ttu-id="421fd-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="421fd-134">NOTES</span></span>

## <span data-ttu-id="421fd-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="421fd-135">RELATED LINKS</span></span>

[<span data-ttu-id="421fd-136">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="421fd-136">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="421fd-137">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="421fd-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="421fd-138">Nowe — AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="421fd-138">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="421fd-139">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="421fd-139">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)
