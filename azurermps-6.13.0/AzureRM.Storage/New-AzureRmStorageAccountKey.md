---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/new-azurermstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
ms.openlocfilehash: e44ccbaae730554db35610ff1084e9740e873e53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553415"
---
# <span data-ttu-id="4e294-101">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4e294-101">New-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="4e294-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4e294-102">SYNOPSIS</span></span>
<span data-ttu-id="4e294-103">Generuje ponownie klucz magazynu dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="4e294-103">Regenerates a storage key for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e294-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4e294-104">SYNTAX</span></span>

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e294-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4e294-105">DESCRIPTION</span></span>
<span data-ttu-id="4e294-106">Polecenie cmdlet **New-AzureRmStorageAccountKey** generuje klucz magazynu dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="4e294-106">The **New-AzureRmStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="4e294-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4e294-107">EXAMPLES</span></span>

### <span data-ttu-id="4e294-108">Przykład 1. Regeneruj klucz magazynu</span><span class="sxs-lookup"><span data-stu-id="4e294-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzureRmStorageKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="4e294-109">To polecenie generuje klucz magazynu dla określonego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="4e294-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="4e294-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4e294-110">PARAMETERS</span></span>

### <span data-ttu-id="4e294-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e294-111">-DefaultProfile</span></span>
<span data-ttu-id="4e294-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4e294-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e294-113">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="4e294-113">-KeyName</span></span>
<span data-ttu-id="4e294-114">Określa klucz, który należy wygenerować.</span><span class="sxs-lookup"><span data-stu-id="4e294-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="4e294-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4e294-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4e294-116">key1</span><span class="sxs-lookup"><span data-stu-id="4e294-116">key1</span></span>
- <span data-ttu-id="4e294-117">key2</span><span class="sxs-lookup"><span data-stu-id="4e294-117">key2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e294-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4e294-118">-Name</span></span>
<span data-ttu-id="4e294-119">Określa nazwę konta magazynu, dla którego ma zostać ponownie wygenerowany klucz magazynu.</span><span class="sxs-lookup"><span data-stu-id="4e294-119">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="4e294-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e294-120">-ResourceGroupName</span></span>
<span data-ttu-id="4e294-121">Określa nazwę grupy zasobów zawierającej konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="4e294-121">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="4e294-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e294-122">CommonParameters</span></span>
<span data-ttu-id="4e294-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e294-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e294-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e294-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e294-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e294-125">INPUTS</span></span>

### <span data-ttu-id="4e294-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4e294-126">System.String</span></span>

## <span data-ttu-id="4e294-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4e294-127">OUTPUTS</span></span>

### <span data-ttu-id="4e294-128">Microsoft. Azure. Management. Storage. MODELES. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4e294-128">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="4e294-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4e294-129">NOTES</span></span>

## <span data-ttu-id="4e294-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4e294-130">RELATED LINKS</span></span>

[<span data-ttu-id="4e294-131">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4e294-131">Get-AzureRmStorageAccountKey</span></span>](./Get-AzureRmStorageAccountKey.md)
