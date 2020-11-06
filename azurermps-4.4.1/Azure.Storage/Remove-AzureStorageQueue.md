---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueue.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 51ea3111b5010b0e29f7bfd69ed5a8e66e596113
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541412"
---
# <span data-ttu-id="8725e-101">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="8725e-101">Remove-AzureStorageQueue</span></span>

## <span data-ttu-id="8725e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8725e-102">SYNOPSIS</span></span>
<span data-ttu-id="8725e-103">Usuwa kolejkę magazynu.</span><span class="sxs-lookup"><span data-stu-id="8725e-103">Removes a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8725e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8725e-104">SYNTAX</span></span>

```
Remove-AzureStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8725e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8725e-105">DESCRIPTION</span></span>
<span data-ttu-id="8725e-106">Polecenie cmdlet **Remove-AzureStorageQueue** umożliwia usunięcie kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="8725e-106">The **Remove-AzureStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="8725e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8725e-107">EXAMPLES</span></span>

### <span data-ttu-id="8725e-108">Przykład 1: usuwanie kolejki magazynu według nazwy</span><span class="sxs-lookup"><span data-stu-id="8725e-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzureStorageQueue "ContosoQueue01"
```

<span data-ttu-id="8725e-109">To polecenie umożliwia usunięcie kolejki o nazwie ContosoQueue01.</span><span class="sxs-lookup"><span data-stu-id="8725e-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="8725e-110">Przykład 2: usuwanie wielu kolejek magazynowania</span><span class="sxs-lookup"><span data-stu-id="8725e-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue "Contoso*" | Remove-AzureStorageQueue
```

<span data-ttu-id="8725e-111">To polecenie usuwa wszystkie kolejki o nazwach rozpoczynających się od contoso.</span><span class="sxs-lookup"><span data-stu-id="8725e-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="8725e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8725e-112">PARAMETERS</span></span>

### <span data-ttu-id="8725e-113">-Context</span><span class="sxs-lookup"><span data-stu-id="8725e-113">-Context</span></span>
<span data-ttu-id="8725e-114">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8725e-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="8725e-115">Aby uzyskać kontekst miejsca do magazynowania, New-AzureStorageContext polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8725e-115">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8725e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8725e-116">-Force</span></span>
<span data-ttu-id="8725e-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8725e-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8725e-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8725e-118">-Name</span></span>
<span data-ttu-id="8725e-119">Określa nazwę kolejki do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="8725e-119">Specifies the name of the queue to remove.</span></span>

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

### <span data-ttu-id="8725e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8725e-120">-PassThru</span></span>
<span data-ttu-id="8725e-121">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="8725e-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="8725e-122">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="8725e-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="8725e-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8725e-123">-Confirm</span></span>
<span data-ttu-id="8725e-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8725e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8725e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8725e-125">-WhatIf</span></span>
<span data-ttu-id="8725e-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8725e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8725e-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8725e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8725e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8725e-128">CommonParameters</span></span>
<span data-ttu-id="8725e-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8725e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8725e-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8725e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8725e-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8725e-131">INPUTS</span></span>

### <span data-ttu-id="8725e-132">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8725e-132">IStorageContext</span></span>

<span data-ttu-id="8725e-133">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="8725e-133">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="8725e-134">Ciąg</span><span class="sxs-lookup"><span data-stu-id="8725e-134">String</span></span>

<span data-ttu-id="8725e-135">Parametr "nazwa" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="8725e-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="8725e-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8725e-136">OUTPUTS</span></span>

### <span data-ttu-id="8725e-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8725e-137">System.Boolean</span></span>

## <span data-ttu-id="8725e-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8725e-138">NOTES</span></span>

## <span data-ttu-id="8725e-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8725e-139">RELATED LINKS</span></span>

[<span data-ttu-id="8725e-140">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="8725e-140">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="8725e-141">Nowe — AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="8725e-141">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)
