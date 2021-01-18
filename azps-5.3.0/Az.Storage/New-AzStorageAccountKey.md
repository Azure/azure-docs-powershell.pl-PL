---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: eebf58120449466ac18231af6daed538ff7da937
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500646"
---
# <span data-ttu-id="89008-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="89008-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="89008-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89008-102">SYNOPSIS</span></span>
<span data-ttu-id="89008-103">Generuje ponownie klucz magazynu dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="89008-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="89008-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89008-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89008-105">Opis</span><span class="sxs-lookup"><span data-stu-id="89008-105">DESCRIPTION</span></span>
<span data-ttu-id="89008-106">Polecenie cmdlet **New-AzStorageAccountKey** generuje klucz magazynu dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="89008-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="89008-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89008-107">EXAMPLES</span></span>

### <span data-ttu-id="89008-108">Przykład 1. Regeneruj klucz magazynu</span><span class="sxs-lookup"><span data-stu-id="89008-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageAccountKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="89008-109">To polecenie generuje klucz magazynu dla określonego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="89008-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="89008-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89008-110">PARAMETERS</span></span>

### <span data-ttu-id="89008-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89008-111">-DefaultProfile</span></span>
<span data-ttu-id="89008-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="89008-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89008-113">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="89008-113">-KeyName</span></span>
<span data-ttu-id="89008-114">Określa klucz, który należy wygenerować.</span><span class="sxs-lookup"><span data-stu-id="89008-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="89008-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="89008-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="89008-116">key1</span><span class="sxs-lookup"><span data-stu-id="89008-116">key1</span></span>
- <span data-ttu-id="89008-117">key2</span><span class="sxs-lookup"><span data-stu-id="89008-117">key2</span></span>
- <span data-ttu-id="89008-118">kerb1</span><span class="sxs-lookup"><span data-stu-id="89008-118">kerb1</span></span>
- <span data-ttu-id="89008-119">kerb2</span><span class="sxs-lookup"><span data-stu-id="89008-119">kerb2</span></span>

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

### <span data-ttu-id="89008-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="89008-120">-Name</span></span>
<span data-ttu-id="89008-121">Określa nazwę konta magazynu, dla którego ma zostać ponownie wygenerowany klucz magazynu.</span><span class="sxs-lookup"><span data-stu-id="89008-121">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="89008-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89008-122">-ResourceGroupName</span></span>
<span data-ttu-id="89008-123">Określa nazwę grupy zasobów zawierającej konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="89008-123">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="89008-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89008-124">CommonParameters</span></span>
<span data-ttu-id="89008-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89008-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89008-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89008-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89008-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89008-127">INPUTS</span></span>

### <span data-ttu-id="89008-128">System. String</span><span class="sxs-lookup"><span data-stu-id="89008-128">System.String</span></span>

## <span data-ttu-id="89008-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89008-129">OUTPUTS</span></span>

### <span data-ttu-id="89008-130">Microsoft. Azure. Management. Storage. MODELES. StorageAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="89008-130">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span></span>

## <span data-ttu-id="89008-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89008-131">NOTES</span></span>

## <span data-ttu-id="89008-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89008-132">RELATED LINKS</span></span>

[<span data-ttu-id="89008-133">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="89008-133">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)
