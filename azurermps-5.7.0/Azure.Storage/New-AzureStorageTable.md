---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
ms.openlocfilehash: 53bb5f3a34cddf9e74bfb9d9c9f1bd1d109d8f6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545868"
---
# <span data-ttu-id="188ff-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="188ff-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="188ff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="188ff-102">SYNOPSIS</span></span>
<span data-ttu-id="188ff-103">Tworzy tabelę magazynu.</span><span class="sxs-lookup"><span data-stu-id="188ff-103">Creates a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="188ff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="188ff-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="188ff-105">Opis</span><span class="sxs-lookup"><span data-stu-id="188ff-105">DESCRIPTION</span></span>
<span data-ttu-id="188ff-106">Polecenie cmdlet **New-AzureStorageTable** tworzy tabelę magazynu skojarzoną z kontem magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="188ff-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="188ff-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="188ff-107">EXAMPLES</span></span>

### <span data-ttu-id="188ff-108">Przykład 1. Tworzenie tabeli magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="188ff-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="188ff-109">To polecenie tworzy tabelę magazynu o nazwie tableabc.</span><span class="sxs-lookup"><span data-stu-id="188ff-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="188ff-110">Przykład 2: Tworzenie wielu tabel magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="188ff-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="188ff-111">To polecenie powoduje utworzenie wielu tabel.</span><span class="sxs-lookup"><span data-stu-id="188ff-111">This command creates multiple tables.</span></span>
<span data-ttu-id="188ff-112">Używa metody **Split** klasy **String** programu .NET, a następnie przekazuje imiona i nazwiska w potoku.</span><span class="sxs-lookup"><span data-stu-id="188ff-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="188ff-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="188ff-113">PARAMETERS</span></span>

### <span data-ttu-id="188ff-114">-Context</span><span class="sxs-lookup"><span data-stu-id="188ff-114">-Context</span></span>
<span data-ttu-id="188ff-115">Określa kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="188ff-115">Specifies the storage context.</span></span>
<span data-ttu-id="188ff-116">Aby ją utworzyć, możesz użyć New-AzureStorageContext polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="188ff-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="188ff-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="188ff-117">-Name</span></span>
<span data-ttu-id="188ff-118">Określa nazwę nowej tabeli.</span><span class="sxs-lookup"><span data-stu-id="188ff-118">Specifies a name for the new table.</span></span>

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

### <span data-ttu-id="188ff-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="188ff-119">CommonParameters</span></span>
<span data-ttu-id="188ff-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="188ff-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="188ff-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="188ff-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="188ff-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="188ff-122">INPUTS</span></span>

### <span data-ttu-id="188ff-123">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="188ff-123">IStorageContext</span></span>

<span data-ttu-id="188ff-124">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="188ff-124">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="188ff-125">Ciąg</span><span class="sxs-lookup"><span data-stu-id="188ff-125">String</span></span>

<span data-ttu-id="188ff-126">Parametr "nazwa" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="188ff-126">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="188ff-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="188ff-127">OUTPUTS</span></span>

### <span data-ttu-id="188ff-128">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="188ff-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="188ff-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="188ff-129">NOTES</span></span>

## <span data-ttu-id="188ff-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="188ff-130">RELATED LINKS</span></span>

[<span data-ttu-id="188ff-131">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="188ff-131">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="188ff-132">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="188ff-132">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


