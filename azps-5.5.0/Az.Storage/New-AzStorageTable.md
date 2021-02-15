---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
ms.openlocfilehash: 0f46570858368a821d176a5f4e0a907c8a56b49c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195730"
---
# <span data-ttu-id="e3767-101">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="e3767-101">New-AzStorageTable</span></span>

## <span data-ttu-id="e3767-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3767-102">SYNOPSIS</span></span>
<span data-ttu-id="e3767-103">Tworzy tabelę magazynu.</span><span class="sxs-lookup"><span data-stu-id="e3767-103">Creates a storage table.</span></span>

## <span data-ttu-id="e3767-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e3767-104">SYNTAX</span></span>

```
New-AzStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3767-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e3767-105">DESCRIPTION</span></span>
<span data-ttu-id="e3767-106">Polecenie **cmdlet New-AzStorageTable** tworzy tabelę magazynu skojarzoną z kontem magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="e3767-106">The **New-AzStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="e3767-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e3767-107">EXAMPLES</span></span>

### <span data-ttu-id="e3767-108">Przykład 1. Tworzenie tabeli magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e3767-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzStorageTable -Name "tableabc"
```

<span data-ttu-id="e3767-109">To polecenie umożliwia utworzenie tabeli magazynu o nazwie tableabc.</span><span class="sxs-lookup"><span data-stu-id="e3767-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="e3767-110">Przykład 2. Tworzenie wielu tabel magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e3767-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzStorageTable
```

<span data-ttu-id="e3767-111">To polecenie umożliwia utworzenie wielu tabel.</span><span class="sxs-lookup"><span data-stu-id="e3767-111">This command creates multiple tables.</span></span>
<span data-ttu-id="e3767-112">Używa metody **Split** klasy .NET **String,** a następnie przekazuje nazwy w potoku.</span><span class="sxs-lookup"><span data-stu-id="e3767-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="e3767-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3767-113">PARAMETERS</span></span>

### <span data-ttu-id="e3767-114">— kontekst</span><span class="sxs-lookup"><span data-stu-id="e3767-114">-Context</span></span>
<span data-ttu-id="e3767-115">Określa kontekst magazynowania.</span><span class="sxs-lookup"><span data-stu-id="e3767-115">Specifies the storage context.</span></span>
<span data-ttu-id="e3767-116">Aby go utworzyć, możesz użyć New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3767-116">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e3767-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3767-117">-DefaultProfile</span></span>
<span data-ttu-id="e3767-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e3767-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3767-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e3767-119">-Name</span></span>
<span data-ttu-id="e3767-120">Określa nazwę nowej tabeli.</span><span class="sxs-lookup"><span data-stu-id="e3767-120">Specifies a name for the new table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3767-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3767-121">CommonParameters</span></span>
<span data-ttu-id="e3767-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3767-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3767-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3767-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3767-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3767-124">INPUTS</span></span>

### <span data-ttu-id="e3767-125">System.String</span><span class="sxs-lookup"><span data-stu-id="e3767-125">System.String</span></span>

### <span data-ttu-id="e3767-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e3767-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e3767-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e3767-127">OUTPUTS</span></span>

### <span data-ttu-id="e3767-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="e3767-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="e3767-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e3767-129">NOTES</span></span>

## <span data-ttu-id="e3767-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3767-130">RELATED LINKS</span></span>

[<span data-ttu-id="e3767-131">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="e3767-131">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)

[<span data-ttu-id="e3767-132">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="e3767-132">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


