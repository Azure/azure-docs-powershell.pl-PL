---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueue.md
ms.openlocfilehash: b98b0ef6e8c4d47c32cab4ee891041e0820ea3ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717770"
---
# <span data-ttu-id="57d0a-101">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="57d0a-101">Remove-AzureStorageQueue</span></span>

## <span data-ttu-id="57d0a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="57d0a-102">SYNOPSIS</span></span>
<span data-ttu-id="57d0a-103">Usuwa kolejkę magazynu.</span><span class="sxs-lookup"><span data-stu-id="57d0a-103">Removes a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57d0a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="57d0a-104">SYNTAX</span></span>

```
Remove-AzureStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57d0a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="57d0a-105">DESCRIPTION</span></span>
<span data-ttu-id="57d0a-106">Polecenie cmdlet **Remove-AzureStorageQueue** umożliwia usunięcie kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="57d0a-106">The **Remove-AzureStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="57d0a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="57d0a-107">EXAMPLES</span></span>

### <span data-ttu-id="57d0a-108">Przykład 1: usuwanie kolejki magazynu według nazwy</span><span class="sxs-lookup"><span data-stu-id="57d0a-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzureStorageQueue "ContosoQueue01"
```

<span data-ttu-id="57d0a-109">To polecenie umożliwia usunięcie kolejki o nazwie ContosoQueue01.</span><span class="sxs-lookup"><span data-stu-id="57d0a-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="57d0a-110">Przykład 2: usuwanie wielu kolejek magazynowania</span><span class="sxs-lookup"><span data-stu-id="57d0a-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue "Contoso*" | Remove-AzureStorageQueue
```

<span data-ttu-id="57d0a-111">To polecenie usuwa wszystkie kolejki o nazwach rozpoczynających się od contoso.</span><span class="sxs-lookup"><span data-stu-id="57d0a-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="57d0a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="57d0a-112">PARAMETERS</span></span>

### <span data-ttu-id="57d0a-113">-Context</span><span class="sxs-lookup"><span data-stu-id="57d0a-113">-Context</span></span>
<span data-ttu-id="57d0a-114">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="57d0a-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="57d0a-115">Aby uzyskać kontekst miejsca do magazynowania, New-AzureStorageContext polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57d0a-115">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="57d0a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="57d0a-116">-Force</span></span>
<span data-ttu-id="57d0a-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="57d0a-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="57d0a-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="57d0a-118">-Name</span></span>
<span data-ttu-id="57d0a-119">Określa nazwę kolejki do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="57d0a-119">Specifies the name of the queue to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57d0a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57d0a-120">-PassThru</span></span>
<span data-ttu-id="57d0a-121">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="57d0a-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="57d0a-122">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="57d0a-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="57d0a-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="57d0a-123">-Confirm</span></span>
<span data-ttu-id="57d0a-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57d0a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57d0a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57d0a-125">-WhatIf</span></span>
<span data-ttu-id="57d0a-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57d0a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57d0a-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="57d0a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57d0a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57d0a-128">CommonParameters</span></span>
<span data-ttu-id="57d0a-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57d0a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57d0a-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57d0a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57d0a-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57d0a-131">INPUTS</span></span>

### <span data-ttu-id="57d0a-132">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="57d0a-132">IStorageContext</span></span>

<span data-ttu-id="57d0a-133">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="57d0a-133">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="57d0a-134">Ciąg</span><span class="sxs-lookup"><span data-stu-id="57d0a-134">String</span></span>

<span data-ttu-id="57d0a-135">Parametr "nazwa" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="57d0a-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="57d0a-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="57d0a-136">OUTPUTS</span></span>

### <span data-ttu-id="57d0a-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="57d0a-137">System.Boolean</span></span>

## <span data-ttu-id="57d0a-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="57d0a-138">NOTES</span></span>

## <span data-ttu-id="57d0a-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57d0a-139">RELATED LINKS</span></span>

[<span data-ttu-id="57d0a-140">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="57d0a-140">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="57d0a-141">Nowe — AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="57d0a-141">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)
