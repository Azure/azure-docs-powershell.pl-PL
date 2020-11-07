---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: 5c575ace97687ca6906a73e8e79d93343f369f45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887877"
---
# <span data-ttu-id="4accc-101">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="4accc-101">Get-AzStorageTable</span></span>

## <span data-ttu-id="4accc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4accc-102">SYNOPSIS</span></span>
<span data-ttu-id="4accc-103">Wyświetla listę tabel magazynu.</span><span class="sxs-lookup"><span data-stu-id="4accc-103">Lists the storage tables.</span></span>

## <span data-ttu-id="4accc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4accc-104">SYNTAX</span></span>

### <span data-ttu-id="4accc-105">Tabelaname (domyślna)</span><span class="sxs-lookup"><span data-stu-id="4accc-105">TableName (Default)</span></span>
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4accc-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="4accc-106">TablePrefix</span></span>
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4accc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4accc-107">DESCRIPTION</span></span>
<span data-ttu-id="4accc-108">Polecenie cmdlet **Get-AzStorageTable** zawiera listę tabel magazynu skojarzonych z kontem magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="4accc-108">The **Get-AzStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="4accc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4accc-109">EXAMPLES</span></span>

### <span data-ttu-id="4accc-110">Przykład 1. Lista wszystkich tabel magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="4accc-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzStorageTable
```

<span data-ttu-id="4accc-111">To polecenie pobiera wszystkie tabele magazynowania dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="4accc-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="4accc-112">Przykład 2: wyświetlanie tabeli magazynu platformy Azure przy użyciu znaku wieloznacznego</span><span class="sxs-lookup"><span data-stu-id="4accc-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzStorageTable -Name table*
```

<span data-ttu-id="4accc-113">To polecenie używa symboli wieloznacznych w celu uzyskania tabel przechowywania, których nazwa zaczyna się od tabeli.</span><span class="sxs-lookup"><span data-stu-id="4accc-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="4accc-114">Przykład 3: Tworzenie listy tabel magazynu platformy Azure przy użyciu prefiksu nazwy tabeli</span><span class="sxs-lookup"><span data-stu-id="4accc-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

<span data-ttu-id="4accc-115">W tym poleceniu jest używany parametr *prefix* umożliwiający pobranie tabel magazynu, których nazwa zaczyna się od tabeli.</span><span class="sxs-lookup"><span data-stu-id="4accc-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="4accc-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4accc-116">PARAMETERS</span></span>

### <span data-ttu-id="4accc-117">-Context</span><span class="sxs-lookup"><span data-stu-id="4accc-117">-Context</span></span>
<span data-ttu-id="4accc-118">Określa kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="4accc-118">Specifies the storage context.</span></span>
<span data-ttu-id="4accc-119">Aby ją utworzyć, możesz użyć New-AzStorageContext polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4accc-119">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4accc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4accc-120">-DefaultProfile</span></span>
<span data-ttu-id="4accc-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4accc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4accc-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4accc-122">-Name</span></span>
<span data-ttu-id="4accc-123">Określa nazwę tabeli.</span><span class="sxs-lookup"><span data-stu-id="4accc-123">Specifies the table name.</span></span>
<span data-ttu-id="4accc-124">Jeśli nazwa tabeli jest pusta, polecenie cmdlet wyświetla wszystkie tabele.</span><span class="sxs-lookup"><span data-stu-id="4accc-124">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="4accc-125">W przeciwnym razie wyświetla wszystkie tabele zgodne z określoną nazwą lub wzorcem zwykłej nazwy.</span><span class="sxs-lookup"><span data-stu-id="4accc-125">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4accc-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="4accc-126">-Prefix</span></span>
<span data-ttu-id="4accc-127">Określa prefiks stosowany w nazwie tabeli lub tabel, które chcesz pobrać.</span><span class="sxs-lookup"><span data-stu-id="4accc-127">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="4accc-128">Za pomocą tej pozycji można znaleźć wszystkie tabele, które zaczynają się od tego samego ciągu, na przykład tabelę.</span><span class="sxs-lookup"><span data-stu-id="4accc-128">You can use this to find all tables that start with the same string, such as table.</span></span>

```yaml
Type: System.String
Parameter Sets: TablePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4accc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4accc-129">CommonParameters</span></span>
<span data-ttu-id="4accc-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4accc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4accc-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4accc-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4accc-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4accc-132">INPUTS</span></span>

### <span data-ttu-id="4accc-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4accc-133">System.String</span></span>

### <span data-ttu-id="4accc-134">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4accc-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4accc-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4accc-135">OUTPUTS</span></span>

### <span data-ttu-id="4accc-136">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="4accc-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="4accc-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4accc-137">NOTES</span></span>

## <span data-ttu-id="4accc-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4accc-138">RELATED LINKS</span></span>

[<span data-ttu-id="4accc-139">Nowe — AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="4accc-139">New-AzStorageTable</span></span>](./New-AzStorageTable.md)

[<span data-ttu-id="4accc-140">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="4accc-140">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


