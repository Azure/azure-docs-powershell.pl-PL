---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/new-azurermstorageaccountkey
schema: 2.0.0
ms.openlocfilehash: 7ea3847c011582d9be809f030a638b09b6cf9532
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897214"
---
# <span data-ttu-id="fb56c-101">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="fb56c-101">New-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="fb56c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fb56c-102">SYNOPSIS</span></span>
<span data-ttu-id="fb56c-103">Generuje ponownie klucz magazynu dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="fb56c-103">Regenerates a storage key for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb56c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fb56c-104">SYNTAX</span></span>

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb56c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fb56c-105">DESCRIPTION</span></span>
<span data-ttu-id="fb56c-106">Polecenie cmdlet **New-AzureRmStorageAccountKey** generuje klucz magazynu dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="fb56c-106">The **New-AzureRmStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="fb56c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fb56c-107">EXAMPLES</span></span>

### <span data-ttu-id="fb56c-108">Przykład 1. Regeneruj klucz magazynu</span><span class="sxs-lookup"><span data-stu-id="fb56c-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzureRmStorageKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="fb56c-109">To polecenie generuje klucz magazynu dla określonego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="fb56c-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="fb56c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fb56c-110">PARAMETERS</span></span>

### <span data-ttu-id="fb56c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb56c-111">-DefaultProfile</span></span>
<span data-ttu-id="fb56c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb56c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb56c-113">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="fb56c-113">-KeyName</span></span>
<span data-ttu-id="fb56c-114">Określa klucz, który należy wygenerować.</span><span class="sxs-lookup"><span data-stu-id="fb56c-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="fb56c-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fb56c-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fb56c-116">key1</span><span class="sxs-lookup"><span data-stu-id="fb56c-116">key1</span></span>
- <span data-ttu-id="fb56c-117">key2</span><span class="sxs-lookup"><span data-stu-id="fb56c-117">key2</span></span>

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

### <span data-ttu-id="fb56c-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fb56c-118">-Name</span></span>
<span data-ttu-id="fb56c-119">Określa nazwę konta magazynu, dla którego ma zostać ponownie wygenerowany klucz magazynu.</span><span class="sxs-lookup"><span data-stu-id="fb56c-119">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="fb56c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb56c-120">-ResourceGroupName</span></span>
<span data-ttu-id="fb56c-121">Określa nazwę grupy zasobów zawierającej konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="fb56c-121">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="fb56c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb56c-122">CommonParameters</span></span>
<span data-ttu-id="fb56c-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb56c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb56c-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb56c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb56c-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb56c-125">INPUTS</span></span>

### <span data-ttu-id="fb56c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fb56c-126">System.String</span></span>

## <span data-ttu-id="fb56c-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fb56c-127">OUTPUTS</span></span>

### <span data-ttu-id="fb56c-128">Microsoft. Azure. Management. Storage. MODELES. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="fb56c-128">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="fb56c-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fb56c-129">NOTES</span></span>

## <span data-ttu-id="fb56c-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb56c-130">RELATED LINKS</span></span>

[<span data-ttu-id="fb56c-131">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="fb56c-131">Get-AzureRmStorageAccountKey</span></span>](./Get-AzureRmStorageAccountKey.md)
