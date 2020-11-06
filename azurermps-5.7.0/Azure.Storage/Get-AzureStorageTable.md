---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
ms.openlocfilehash: ac25103ed8a933af4e118087371511842044b6a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545899"
---
# <span data-ttu-id="ff12e-101">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="ff12e-101">Get-AzureStorageTable</span></span>

## <span data-ttu-id="ff12e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ff12e-102">SYNOPSIS</span></span>
<span data-ttu-id="ff12e-103">Wyświetla listę tabel magazynu.</span><span class="sxs-lookup"><span data-stu-id="ff12e-103">Lists the storage tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff12e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ff12e-104">SYNTAX</span></span>

### <span data-ttu-id="ff12e-105">Tabelaname (domyślna)</span><span class="sxs-lookup"><span data-stu-id="ff12e-105">TableName (Default)</span></span>
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="ff12e-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="ff12e-106">TablePrefix</span></span>
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="ff12e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ff12e-107">DESCRIPTION</span></span>
<span data-ttu-id="ff12e-108">Polecenie cmdlet **Get-AzureStorageTable** zawiera listę tabel magazynu skojarzonych z kontem magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="ff12e-108">The **Get-AzureStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="ff12e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ff12e-109">EXAMPLES</span></span>

### <span data-ttu-id="ff12e-110">Przykład 1. Lista wszystkich tabel magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ff12e-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzureStorageTable
```

<span data-ttu-id="ff12e-111">To polecenie pobiera wszystkie tabele magazynowania dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ff12e-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="ff12e-112">Przykład 2: wyświetlanie tabeli magazynu platformy Azure przy użyciu znaku wieloznacznego</span><span class="sxs-lookup"><span data-stu-id="ff12e-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageTable -Name table*
```

<span data-ttu-id="ff12e-113">To polecenie używa symboli wieloznacznych w celu uzyskania tabel przechowywania, których nazwa zaczyna się od tabeli.</span><span class="sxs-lookup"><span data-stu-id="ff12e-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="ff12e-114">Przykład 3: Tworzenie listy tabel magazynu platformy Azure przy użyciu prefiksu nazwy tabeli</span><span class="sxs-lookup"><span data-stu-id="ff12e-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

<span data-ttu-id="ff12e-115">W tym poleceniu jest używany parametr *prefix* umożliwiający pobranie tabel magazynu, których nazwa zaczyna się od tabeli.</span><span class="sxs-lookup"><span data-stu-id="ff12e-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="ff12e-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ff12e-116">PARAMETERS</span></span>

### <span data-ttu-id="ff12e-117">-Context</span><span class="sxs-lookup"><span data-stu-id="ff12e-117">-Context</span></span>
<span data-ttu-id="ff12e-118">Określa kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="ff12e-118">Specifies the storage context.</span></span>
<span data-ttu-id="ff12e-119">Aby ją utworzyć, możesz użyć New-AzureStorageContext polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff12e-119">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ff12e-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ff12e-120">-Name</span></span>
<span data-ttu-id="ff12e-121">Określa nazwę tabeli.</span><span class="sxs-lookup"><span data-stu-id="ff12e-121">Specifies the table name.</span></span>
<span data-ttu-id="ff12e-122">Jeśli nazwa tabeli jest pusta, polecenie cmdlet wyświetla wszystkie tabele.</span><span class="sxs-lookup"><span data-stu-id="ff12e-122">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="ff12e-123">W przeciwnym razie wyświetla wszystkie tabele zgodne z określoną nazwą lub wzorcem zwykłej nazwy.</span><span class="sxs-lookup"><span data-stu-id="ff12e-123">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="ff12e-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="ff12e-124">-Prefix</span></span>
<span data-ttu-id="ff12e-125">Określa prefiks stosowany w nazwie tabeli lub tabel, które chcesz pobrać.</span><span class="sxs-lookup"><span data-stu-id="ff12e-125">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="ff12e-126">Za pomocą tej pozycji można znaleźć wszystkie tabele, które zaczynają się od tego samego ciągu, na przykład tabelę.</span><span class="sxs-lookup"><span data-stu-id="ff12e-126">You can use this to find all tables that start with the same string, such as table.</span></span>

```yaml
Type: String
Parameter Sets: TablePrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff12e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff12e-127">CommonParameters</span></span>
<span data-ttu-id="ff12e-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff12e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff12e-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff12e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff12e-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff12e-130">INPUTS</span></span>

### <span data-ttu-id="ff12e-131">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ff12e-131">IStorageContext</span></span>

<span data-ttu-id="ff12e-132">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="ff12e-132">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="ff12e-133">Ciąg</span><span class="sxs-lookup"><span data-stu-id="ff12e-133">String</span></span>

<span data-ttu-id="ff12e-134">Parametr "nazwa" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="ff12e-134">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="ff12e-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ff12e-135">OUTPUTS</span></span>

### <span data-ttu-id="ff12e-136">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="ff12e-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="ff12e-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ff12e-137">NOTES</span></span>

## <span data-ttu-id="ff12e-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff12e-138">RELATED LINKS</span></span>

[<span data-ttu-id="ff12e-139">Nowe — AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="ff12e-139">New-AzureStorageTable</span></span>](./New-AzureStorageTable.md)

[<span data-ttu-id="ff12e-140">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="ff12e-140">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


