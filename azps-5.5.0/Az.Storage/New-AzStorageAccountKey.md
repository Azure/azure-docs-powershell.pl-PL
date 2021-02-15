---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: eebf58120449466ac18231af6daed538ff7da937
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195755"
---
# <span data-ttu-id="f5ac0-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f5ac0-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="f5ac0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5ac0-102">SYNOPSIS</span></span>
<span data-ttu-id="f5ac0-103">Ponowne generowanie klucza magazynu dla konta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f5ac0-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="f5ac0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f5ac0-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5ac0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f5ac0-105">DESCRIPTION</span></span>
<span data-ttu-id="f5ac0-106">Polecenie **cmdlet New-AzStorageAccountKey** ponownie generuje klucz magazynu dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="f5ac0-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="f5ac0-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f5ac0-107">EXAMPLES</span></span>

### <span data-ttu-id="f5ac0-108">Przykład 1. Ponowne generowanie klucza magazynu</span><span class="sxs-lookup"><span data-stu-id="f5ac0-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageAccountKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="f5ac0-109">To polecenie ponownie generuje klucz magazynu dla określonego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="f5ac0-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="f5ac0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5ac0-110">PARAMETERS</span></span>

### <span data-ttu-id="f5ac0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5ac0-111">-DefaultProfile</span></span>
<span data-ttu-id="f5ac0-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f5ac0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5ac0-113">-KeyName</span><span class="sxs-lookup"><span data-stu-id="f5ac0-113">-KeyName</span></span>
<span data-ttu-id="f5ac0-114">Określa klucz do ponownego wygenerowania.</span><span class="sxs-lookup"><span data-stu-id="f5ac0-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="f5ac0-115">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f5ac0-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f5ac0-116">klawisz1</span><span class="sxs-lookup"><span data-stu-id="f5ac0-116">key1</span></span>
- <span data-ttu-id="f5ac0-117">klawisz 2</span><span class="sxs-lookup"><span data-stu-id="f5ac0-117">key2</span></span>
- <span data-ttu-id="f5ac0-118">kerb1</span><span class="sxs-lookup"><span data-stu-id="f5ac0-118">kerb1</span></span>
- <span data-ttu-id="f5ac0-119">kerb2</span><span class="sxs-lookup"><span data-stu-id="f5ac0-119">kerb2</span></span>

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

### <span data-ttu-id="f5ac0-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f5ac0-120">-Name</span></span>
<span data-ttu-id="f5ac0-121">Określa nazwę konta magazynu, dla którego ma być ponownie wygenerowany klucz magazynu.</span><span class="sxs-lookup"><span data-stu-id="f5ac0-121">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="f5ac0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5ac0-122">-ResourceGroupName</span></span>
<span data-ttu-id="f5ac0-123">Określa nazwę grupy zasobów zawierającej konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="f5ac0-123">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="f5ac0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5ac0-124">CommonParameters</span></span>
<span data-ttu-id="f5ac0-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5ac0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5ac0-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5ac0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5ac0-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5ac0-127">INPUTS</span></span>

### <span data-ttu-id="f5ac0-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f5ac0-128">System.String</span></span>

## <span data-ttu-id="f5ac0-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f5ac0-129">OUTPUTS</span></span>

### <span data-ttu-id="f5ac0-130">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="f5ac0-130">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span></span>

## <span data-ttu-id="f5ac0-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f5ac0-131">NOTES</span></span>

## <span data-ttu-id="f5ac0-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5ac0-132">RELATED LINKS</span></span>

[<span data-ttu-id="f5ac0-133">Get-AzstorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f5ac0-133">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)
