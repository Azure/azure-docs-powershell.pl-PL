---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: d501faaebcc5e381dc2a7270c8b55b148e2812b4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195794"
---
# <span data-ttu-id="a22b4-101">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="a22b4-101">Get-AzStorageTable</span></span>

## <span data-ttu-id="a22b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a22b4-102">SYNOPSIS</span></span>
<span data-ttu-id="a22b4-103">Wyświetla listę tabel magazynu.</span><span class="sxs-lookup"><span data-stu-id="a22b4-103">Lists the storage tables.</span></span>

## <span data-ttu-id="a22b4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a22b4-104">SYNTAX</span></span>

### <span data-ttu-id="a22b4-105">Nazwa_tabeli (domyślna)</span><span class="sxs-lookup"><span data-stu-id="a22b4-105">TableName (Default)</span></span>
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a22b4-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="a22b4-106">TablePrefix</span></span>
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a22b4-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a22b4-107">DESCRIPTION</span></span>
<span data-ttu-id="a22b4-108">Polecenie **cmdlet Get-AzStorageTable** wyświetla listę tabel magazynu skojarzonych z kontem magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="a22b4-108">The **Get-AzStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="a22b4-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a22b4-109">EXAMPLES</span></span>

### <span data-ttu-id="a22b4-110">Przykład 1. Lista wszystkich tabel magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="a22b4-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzStorageTable
```

<span data-ttu-id="a22b4-111">To polecenie pobiera wszystkie tabele magazynu dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="a22b4-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="a22b4-112">Przykład 2. Lista tabel magazynu platformy Azure przy użyciu symboli wieloznacznych</span><span class="sxs-lookup"><span data-stu-id="a22b4-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzStorageTable -Name table*
```

<span data-ttu-id="a22b4-113">To polecenie używa symbolu wieloznacznego w celu uzyskania tabel magazynu, których nazwa zaczyna się od tabeli.</span><span class="sxs-lookup"><span data-stu-id="a22b4-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="a22b4-114">Przykład 3. Lista tabel magazynu platformy Azure przy użyciu prefiksu nazwy tabeli</span><span class="sxs-lookup"><span data-stu-id="a22b4-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

<span data-ttu-id="a22b4-115">To polecenie używa *parametru Prefiks* w celu uzyskania tabel magazynu, których nazwa zaczyna się od tabeli.</span><span class="sxs-lookup"><span data-stu-id="a22b4-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="a22b4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a22b4-116">PARAMETERS</span></span>

### <span data-ttu-id="a22b4-117">— kontekst</span><span class="sxs-lookup"><span data-stu-id="a22b4-117">-Context</span></span>
<span data-ttu-id="a22b4-118">Określa kontekst magazynowania.</span><span class="sxs-lookup"><span data-stu-id="a22b4-118">Specifies the storage context.</span></span>
<span data-ttu-id="a22b4-119">Aby go utworzyć, możesz użyć New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a22b4-119">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a22b4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a22b4-120">-DefaultProfile</span></span>
<span data-ttu-id="a22b4-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a22b4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a22b4-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a22b4-122">-Name</span></span>
<span data-ttu-id="a22b4-123">Określa nazwę tabeli.</span><span class="sxs-lookup"><span data-stu-id="a22b4-123">Specifies the table name.</span></span>
<span data-ttu-id="a22b4-124">Jeśli nazwa tabeli jest pusta, polecenie cmdlet wyświetla listę wszystkich tabel.</span><span class="sxs-lookup"><span data-stu-id="a22b4-124">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="a22b4-125">W przeciwnym razie wyświetla listę wszystkich tabel, które pasują do określonej nazwy lub wzorca nazw zwykłych.</span><span class="sxs-lookup"><span data-stu-id="a22b4-125">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

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

### <span data-ttu-id="a22b4-126">—Prefiks</span><span class="sxs-lookup"><span data-stu-id="a22b4-126">-Prefix</span></span>
<span data-ttu-id="a22b4-127">Określa prefiks używany w nazwie tabeli lub tabel, które chcesz uzyskać.</span><span class="sxs-lookup"><span data-stu-id="a22b4-127">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="a22b4-128">Dzięki temu można znaleźć wszystkie tabele, które zaczynają się od tego samego ciągu znaków, na przykład tabelę.</span><span class="sxs-lookup"><span data-stu-id="a22b4-128">You can use this to find all tables that start with the same string, such as table.</span></span>

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

### <span data-ttu-id="a22b4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a22b4-129">CommonParameters</span></span>
<span data-ttu-id="a22b4-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a22b4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a22b4-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a22b4-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a22b4-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a22b4-132">INPUTS</span></span>

### <span data-ttu-id="a22b4-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a22b4-133">System.String</span></span>

### <span data-ttu-id="a22b4-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a22b4-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a22b4-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a22b4-135">OUTPUTS</span></span>

### <span data-ttu-id="a22b4-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="a22b4-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="a22b4-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a22b4-137">NOTES</span></span>

## <span data-ttu-id="a22b4-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a22b4-138">RELATED LINKS</span></span>

[<span data-ttu-id="a22b4-139">New-azstorageTable</span><span class="sxs-lookup"><span data-stu-id="a22b4-139">New-AzStorageTable</span></span>](./New-AzStorageTable.md)

[<span data-ttu-id="a22b4-140">Remove-azstorageTable</span><span class="sxs-lookup"><span data-stu-id="a22b4-140">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


