---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTable.md
ms.openlocfilehash: 7423cbb6995430523beb137ef10eb6f1a53c959c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717539"
---
# <span data-ttu-id="bbad3-101">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="bbad3-101">Remove-AzureStorageTable</span></span>

## <span data-ttu-id="bbad3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bbad3-102">SYNOPSIS</span></span>
<span data-ttu-id="bbad3-103">Usuwa tabelę magazynu.</span><span class="sxs-lookup"><span data-stu-id="bbad3-103">Removes a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbad3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bbad3-104">SYNTAX</span></span>

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbad3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bbad3-105">DESCRIPTION</span></span>
<span data-ttu-id="bbad3-106">Polecenie cmdlet **Remove-AzureStorageTable** usuwa co najmniej jeden magazyn z konta magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="bbad3-106">The **Remove-AzureStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="bbad3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bbad3-107">EXAMPLES</span></span>

### <span data-ttu-id="bbad3-108">Przykład 1. Usuwanie tabeli</span><span class="sxs-lookup"><span data-stu-id="bbad3-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

<span data-ttu-id="bbad3-109">To polecenie umożliwia usunięcie tabeli.</span><span class="sxs-lookup"><span data-stu-id="bbad3-109">This command removes a table.</span></span>

### <span data-ttu-id="bbad3-110">Przykład 2: Usuwanie kilku tabel</span><span class="sxs-lookup"><span data-stu-id="bbad3-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

<span data-ttu-id="bbad3-111">W tym przykładzie użyto symbolu wieloznacznego z parametrem *name* w celu uzyskania wszystkich tabel pasujących do tabeli wzorzec, a następnie przekazanie wyniku w potoku w celu usunięcia tabel.</span><span class="sxs-lookup"><span data-stu-id="bbad3-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="bbad3-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bbad3-112">PARAMETERS</span></span>

### <span data-ttu-id="bbad3-113">-Context</span><span class="sxs-lookup"><span data-stu-id="bbad3-113">-Context</span></span>
<span data-ttu-id="bbad3-114">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="bbad3-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="bbad3-115">Możesz ją utworzyć przy użyciu polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="bbad3-115">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="bbad3-116">-Force</span><span class="sxs-lookup"><span data-stu-id="bbad3-116">-Force</span></span>
<span data-ttu-id="bbad3-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="bbad3-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bbad3-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bbad3-118">-Name</span></span>
<span data-ttu-id="bbad3-119">Określa nazwę tabeli, która ma zostać usunięta.</span><span class="sxs-lookup"><span data-stu-id="bbad3-119">Specifies the name of the table to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbad3-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bbad3-120">-PassThru</span></span>
<span data-ttu-id="bbad3-121">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="bbad3-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="bbad3-122">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="bbad3-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="bbad3-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bbad3-123">-Confirm</span></span>
<span data-ttu-id="bbad3-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbad3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbad3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbad3-125">-WhatIf</span></span>
<span data-ttu-id="bbad3-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbad3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbad3-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bbad3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbad3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbad3-128">CommonParameters</span></span>
<span data-ttu-id="bbad3-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbad3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbad3-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbad3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbad3-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bbad3-131">INPUTS</span></span>

### <span data-ttu-id="bbad3-132">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bbad3-132">IStorageContext</span></span>

<span data-ttu-id="bbad3-133">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="bbad3-133">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="bbad3-134">Ciąg</span><span class="sxs-lookup"><span data-stu-id="bbad3-134">String</span></span>

<span data-ttu-id="bbad3-135">Parametr "nazwa" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="bbad3-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="bbad3-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bbad3-136">OUTPUTS</span></span>

### <span data-ttu-id="bbad3-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bbad3-137">System.Boolean</span></span>

## <span data-ttu-id="bbad3-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bbad3-138">NOTES</span></span>

## <span data-ttu-id="bbad3-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bbad3-139">RELATED LINKS</span></span>

[<span data-ttu-id="bbad3-140">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="bbad3-140">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)
