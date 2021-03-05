---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: 254d9a012bd3539242e560511e23975acb68b4bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002657"
---
# <span data-ttu-id="899a8-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="899a8-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="899a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="899a8-102">SYNOPSIS</span></span>
<span data-ttu-id="899a8-103">Ponowne generowanie klucza magazynu dla konta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="899a8-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="899a8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="899a8-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="899a8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="899a8-105">DESCRIPTION</span></span>
<span data-ttu-id="899a8-106">Polecenie **cmdlet New-AzStorageAccountKey** ponownie generuje klucz magazynu dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="899a8-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="899a8-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="899a8-107">EXAMPLES</span></span>

### <span data-ttu-id="899a8-108">Przykład 1. Ponowne generowanie klucza magazynu</span><span class="sxs-lookup"><span data-stu-id="899a8-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageAccountKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="899a8-109">To polecenie ponownie generuje klucz magazynu dla określonego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="899a8-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="899a8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="899a8-110">PARAMETERS</span></span>

### <span data-ttu-id="899a8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="899a8-111">-DefaultProfile</span></span>
<span data-ttu-id="899a8-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="899a8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="899a8-113">-KeyName</span><span class="sxs-lookup"><span data-stu-id="899a8-113">-KeyName</span></span>
<span data-ttu-id="899a8-114">Określa klucz do ponownego wygenerowania.</span><span class="sxs-lookup"><span data-stu-id="899a8-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="899a8-115">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="899a8-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="899a8-116">klawisz1</span><span class="sxs-lookup"><span data-stu-id="899a8-116">key1</span></span>
- <span data-ttu-id="899a8-117">klawisz 2</span><span class="sxs-lookup"><span data-stu-id="899a8-117">key2</span></span>
- <span data-ttu-id="899a8-118">kerb1</span><span class="sxs-lookup"><span data-stu-id="899a8-118">kerb1</span></span>
- <span data-ttu-id="899a8-119">kerb2</span><span class="sxs-lookup"><span data-stu-id="899a8-119">kerb2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2, kerb1, kerb2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="899a8-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="899a8-120">-Name</span></span>
<span data-ttu-id="899a8-121">Określa nazwę konta magazynu, dla którego ma być ponownie wygenerowany klucz magazynu.</span><span class="sxs-lookup"><span data-stu-id="899a8-121">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="899a8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="899a8-122">-ResourceGroupName</span></span>
<span data-ttu-id="899a8-123">Określa nazwę grupy zasobów zawierającej konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="899a8-123">Specifies the name of the resource group that contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="899a8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="899a8-124">CommonParameters</span></span>
<span data-ttu-id="899a8-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="899a8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="899a8-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="899a8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="899a8-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="899a8-127">INPUTS</span></span>

### <span data-ttu-id="899a8-128">System.String</span><span class="sxs-lookup"><span data-stu-id="899a8-128">System.String</span></span>

## <span data-ttu-id="899a8-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="899a8-129">OUTPUTS</span></span>

### <span data-ttu-id="899a8-130">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="899a8-130">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span></span>

## <span data-ttu-id="899a8-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="899a8-131">NOTES</span></span>

## <span data-ttu-id="899a8-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="899a8-132">RELATED LINKS</span></span>

[<span data-ttu-id="899a8-133">Get-AzstorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="899a8-133">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)
