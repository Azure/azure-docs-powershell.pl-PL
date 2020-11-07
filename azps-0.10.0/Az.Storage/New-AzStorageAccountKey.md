---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: 70acc17513e60892baae1fe8ebc15776518b3f57
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892182"
---
# <span data-ttu-id="8856d-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="8856d-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="8856d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8856d-102">SYNOPSIS</span></span>
<span data-ttu-id="8856d-103">Generuje ponownie klucz magazynu dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8856d-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="8856d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8856d-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8856d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8856d-105">DESCRIPTION</span></span>
<span data-ttu-id="8856d-106">Polecenie cmdlet **New-AzStorageAccountKey** generuje klucz magazynu dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8856d-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="8856d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8856d-107">EXAMPLES</span></span>

### <span data-ttu-id="8856d-108">Przykład 1. Regeneruj klucz magazynu</span><span class="sxs-lookup"><span data-stu-id="8856d-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="8856d-109">To polecenie generuje klucz magazynu dla określonego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="8856d-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="8856d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8856d-110">PARAMETERS</span></span>

### <span data-ttu-id="8856d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8856d-111">-DefaultProfile</span></span>
<span data-ttu-id="8856d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8856d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8856d-113">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="8856d-113">-KeyName</span></span>
<span data-ttu-id="8856d-114">Określa klucz, który należy wygenerować.</span><span class="sxs-lookup"><span data-stu-id="8856d-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="8856d-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8856d-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8856d-116">key1</span><span class="sxs-lookup"><span data-stu-id="8856d-116">key1</span></span>
- <span data-ttu-id="8856d-117">key2</span><span class="sxs-lookup"><span data-stu-id="8856d-117">key2</span></span>

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

### <span data-ttu-id="8856d-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8856d-118">-Name</span></span>
<span data-ttu-id="8856d-119">Określa nazwę konta magazynu, dla którego ma zostać ponownie wygenerowany klucz magazynu.</span><span class="sxs-lookup"><span data-stu-id="8856d-119">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="8856d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8856d-120">-ResourceGroupName</span></span>
<span data-ttu-id="8856d-121">Określa nazwę grupy zasobów zawierającej konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="8856d-121">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="8856d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8856d-122">CommonParameters</span></span>
<span data-ttu-id="8856d-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8856d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8856d-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8856d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8856d-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8856d-125">INPUTS</span></span>

### <span data-ttu-id="8856d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8856d-126">System.String</span></span>

## <span data-ttu-id="8856d-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8856d-127">OUTPUTS</span></span>

### <span data-ttu-id="8856d-128">Microsoft. Azure. Management. Storage. MODELES. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="8856d-128">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="8856d-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8856d-129">NOTES</span></span>

## <span data-ttu-id="8856d-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8856d-130">RELATED LINKS</span></span>

[<span data-ttu-id="8856d-131">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="8856d-131">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)
