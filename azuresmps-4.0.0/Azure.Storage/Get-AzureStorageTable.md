---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f2bccab190fc27b5e97ecf3af502d3488f28998
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523994"
---
# <span data-ttu-id="fc0bc-101">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="fc0bc-101">Get-AzureStorageTable</span></span>

## <span data-ttu-id="fc0bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fc0bc-102">SYNOPSIS</span></span>
<span data-ttu-id="fc0bc-103">Wyświetla listę tabel magazynu.</span><span class="sxs-lookup"><span data-stu-id="fc0bc-103">Lists the storage tables.</span></span>

## <span data-ttu-id="fc0bc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fc0bc-104">SYNTAX</span></span>

### <span data-ttu-id="fc0bc-105">Tabelaname (domyślna)</span><span class="sxs-lookup"><span data-stu-id="fc0bc-105">TableName (Default)</span></span>
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="fc0bc-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="fc0bc-106">TablePrefix</span></span>
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="fc0bc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fc0bc-107">DESCRIPTION</span></span>
<span data-ttu-id="fc0bc-108">Polecenie cmdlet **Get-AzureStorageTable** zawiera listę tabel magazynu skojarzonych z kontem magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="fc0bc-108">The **Get-AzureStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="fc0bc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fc0bc-109">EXAMPLES</span></span>

### <span data-ttu-id="fc0bc-110">Przykład 1. Lista wszystkich tabel magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="fc0bc-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzureStorageTable
```

<span data-ttu-id="fc0bc-111">To polecenie pobiera wszystkie tabele magazynowania dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="fc0bc-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="fc0bc-112">Przykład 2: wyświetlanie tabeli magazynu platformy Azure przy użyciu znaku wieloznacznego</span><span class="sxs-lookup"><span data-stu-id="fc0bc-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageTable -Name table*
```

<span data-ttu-id="fc0bc-113">To polecenie używa symboli wieloznacznych w celu uzyskania tabel przechowywania, których nazwa zaczyna się od tabeli.</span><span class="sxs-lookup"><span data-stu-id="fc0bc-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="fc0bc-114">Przykład 3: Tworzenie listy tabel magazynu platformy Azure przy użyciu prefiksu nazwy tabeli</span><span class="sxs-lookup"><span data-stu-id="fc0bc-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

<span data-ttu-id="fc0bc-115">W tym poleceniu jest używany parametr *prefix* umożliwiający pobranie tabel magazynu, których nazwa zaczyna się od tabeli.</span><span class="sxs-lookup"><span data-stu-id="fc0bc-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="fc0bc-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fc0bc-116">PARAMETERS</span></span>

### <span data-ttu-id="fc0bc-117">-Context</span><span class="sxs-lookup"><span data-stu-id="fc0bc-117">-Context</span></span>
<span data-ttu-id="fc0bc-118">Określa kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="fc0bc-118">Specifies the storage context.</span></span>
<span data-ttu-id="fc0bc-119">Aby ją utworzyć, możesz użyć New-AzureStorageContext polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc0bc-119">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fc0bc-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fc0bc-120">-Name</span></span>
<span data-ttu-id="fc0bc-121">Określa nazwę tabeli.</span><span class="sxs-lookup"><span data-stu-id="fc0bc-121">Specifies the table name.</span></span>
<span data-ttu-id="fc0bc-122">Jeśli nazwa tabeli jest pusta, polecenie cmdlet wyświetla wszystkie tabele.</span><span class="sxs-lookup"><span data-stu-id="fc0bc-122">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="fc0bc-123">W przeciwnym razie wyświetla wszystkie tabele zgodne z określoną nazwą lub wzorcem zwykłej nazwy.</span><span class="sxs-lookup"><span data-stu-id="fc0bc-123">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0bc-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="fc0bc-124">-Prefix</span></span>
<span data-ttu-id="fc0bc-125">Określa prefiks stosowany w nazwie tabeli lub tabel, które chcesz pobrać.</span><span class="sxs-lookup"><span data-stu-id="fc0bc-125">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="fc0bc-126">Za pomocą tej pozycji można znaleźć wszystkie tabele, które zaczynają się od tego samego ciągu, na przykład tabelę.</span><span class="sxs-lookup"><span data-stu-id="fc0bc-126">You can use this to find all tables that start with the same string, such as table.</span></span>

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

### <span data-ttu-id="fc0bc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc0bc-127">CommonParameters</span></span>
<span data-ttu-id="fc0bc-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc0bc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc0bc-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc0bc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc0bc-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc0bc-130">INPUTS</span></span>

## <span data-ttu-id="fc0bc-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fc0bc-131">OUTPUTS</span></span>

## <span data-ttu-id="fc0bc-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fc0bc-132">NOTES</span></span>

## <span data-ttu-id="fc0bc-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc0bc-133">RELATED LINKS</span></span>

[<span data-ttu-id="fc0bc-134">Nowe — AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="fc0bc-134">New-AzureStorageTable</span></span>](./New-AzureStorageTable.md)

[<span data-ttu-id="fc0bc-135">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="fc0bc-135">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


