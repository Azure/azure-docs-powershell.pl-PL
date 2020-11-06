---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
ms.openlocfilehash: e84bb0dd511f5534b8794327b68f2321efcdc130
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526525"
---
# <span data-ttu-id="4a057-101">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4a057-101">Get-AzureRmStorageAccount</span></span>

## <span data-ttu-id="4a057-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4a057-102">SYNOPSIS</span></span>
<span data-ttu-id="4a057-103">Pobiera konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="4a057-103">Gets a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a057-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4a057-104">SYNTAX</span></span>

### <span data-ttu-id="4a057-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a057-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmStorageAccount [[-ResourceGroupName] <String>] [<CommonParameters>]
```

### <span data-ttu-id="4a057-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a057-106">AccountNameParameterSet</span></span>
```
Get-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="4a057-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4a057-107">DESCRIPTION</span></span>
<span data-ttu-id="4a057-108">Polecenie cmdlet **Get-AzureRmStorageAccount** pobiera określone konto magazynu lub wszystkie konta magazynu w grupie zasobów lub abonament.</span><span class="sxs-lookup"><span data-stu-id="4a057-108">The **Get-AzureRmStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="4a057-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4a057-109">EXAMPLES</span></span>

### <span data-ttu-id="4a057-110">Przykład 1: uzyskiwanie określonego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="4a057-110">Example 1: Get a specified storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="4a057-111">To polecenie pobiera określone konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="4a057-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="4a057-112">Przykład 2: pobieranie wszystkich kont magazynu w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="4a057-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="4a057-113">To polecenie umożliwia pobieranie wszystkich kont magazynu w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="4a057-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="4a057-114">Przykład 3: uzyskiwanie wszystkich kont magazynu w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="4a057-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzureRmStorageAccount
```

<span data-ttu-id="4a057-115">To polecenie umożliwia pobieranie wszystkich kont magazynu w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="4a057-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="4a057-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4a057-116">PARAMETERS</span></span>

### <span data-ttu-id="4a057-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4a057-117">-Name</span></span>
<span data-ttu-id="4a057-118">Określa nazwę konta magazynu, które ma zostać pozyskane.</span><span class="sxs-lookup"><span data-stu-id="4a057-118">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a057-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a057-119">-ResourceGroupName</span></span>
<span data-ttu-id="4a057-120">Określa nazwę grupy zasobów zawierającej konto magazynu do pobrania.</span><span class="sxs-lookup"><span data-stu-id="4a057-120">Specifies the name of the resource group that contains the Storage account to get.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a057-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a057-121">CommonParameters</span></span>
<span data-ttu-id="4a057-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a057-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a057-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a057-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a057-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a057-124">INPUTS</span></span>

### <span data-ttu-id="4a057-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4a057-125">None</span></span>
<span data-ttu-id="4a057-126">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="4a057-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4a057-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4a057-127">OUTPUTS</span></span>

## <span data-ttu-id="4a057-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4a057-128">NOTES</span></span>

## <span data-ttu-id="4a057-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a057-129">RELATED LINKS</span></span>

[<span data-ttu-id="4a057-130">Nowe — AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4a057-130">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="4a057-131">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4a057-131">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="4a057-132">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4a057-132">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)
