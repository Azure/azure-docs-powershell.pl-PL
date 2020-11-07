---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
ms.openlocfilehash: ed44fa5960935bbe353d775a426e023512327e7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717241"
---
# <span data-ttu-id="4e25b-101">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="4e25b-101">New-AzureRmBatchAccount</span></span>

## <span data-ttu-id="4e25b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4e25b-102">SYNOPSIS</span></span>
<span data-ttu-id="4e25b-103">Tworzy konto wsadowe.</span><span class="sxs-lookup"><span data-stu-id="4e25b-103">Creates a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e25b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4e25b-104">SYNTAX</span></span>

```
New-AzureRmBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e25b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4e25b-105">DESCRIPTION</span></span>
<span data-ttu-id="4e25b-106">Polecenie cmdlet **New-AzureRmBatchAccount** tworzy konto usługi Azure Batch dla określonej grupy zasobów i lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="4e25b-106">The **New-AzureRmBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="4e25b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4e25b-107">EXAMPLES</span></span>

### <span data-ttu-id="4e25b-108">Przykład 1. Tworzenie konta wsadowego</span><span class="sxs-lookup"><span data-stu-id="4e25b-108">Example 1: Create a Batch account</span></span>
```
PS C:\>New-AzureRmBatchAccount -AccountName "pfuller" -ResourceGroupName "ResourceGroup03" -Location "WestUS"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : ResourceGroup03
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="4e25b-109">To polecenie tworzy konto wsadowe o nazwie pfuller przy użyciu ResourceGroup03 grupy zasobów w zachodniej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="4e25b-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="4e25b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4e25b-110">PARAMETERS</span></span>

### <span data-ttu-id="4e25b-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4e25b-111">-AccountName</span></span>
<span data-ttu-id="4e25b-112">Określa nazwę konta wsadowego tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e25b-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>

<span data-ttu-id="4e25b-113">Nazwy kont wsadowych muszą mieć od 3 do 24 znaków i zawierać tylko cyfry i małe litery.</span><span class="sxs-lookup"><span data-stu-id="4e25b-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e25b-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4e25b-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="4e25b-115">Określa identyfikator zasobu konta magazynu, który ma być wykorzystywany do automatycznego przechowywania danych.</span><span class="sxs-lookup"><span data-stu-id="4e25b-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e25b-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4e25b-116">-Location</span></span>
<span data-ttu-id="4e25b-117">Określa region, w którym to polecenie cmdlet tworzy konto.</span><span class="sxs-lookup"><span data-stu-id="4e25b-117">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="4e25b-118">Aby uzyskać więcej informacji, zobacz [regiony platformy Azure](https://azure.microsoft.com/en-us/regions).</span><span class="sxs-lookup"><span data-stu-id="4e25b-118">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e25b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e25b-119">-ResourceGroupName</span></span>
<span data-ttu-id="4e25b-120">Określa nazwę grupy zasobów, w której to polecenie cmdlet tworzy konto.</span><span class="sxs-lookup"><span data-stu-id="4e25b-120">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e25b-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="4e25b-121">-Tag</span></span>
<span data-ttu-id="4e25b-122">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="4e25b-122">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4e25b-123">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="4e25b-123">For example:</span></span>

<span data-ttu-id="4e25b-124">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="4e25b-124">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e25b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e25b-125">-DefaultProfile</span></span>
<span data-ttu-id="4e25b-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4e25b-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e25b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e25b-127">CommonParameters</span></span>
<span data-ttu-id="4e25b-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e25b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e25b-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e25b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e25b-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e25b-130">INPUTS</span></span>

## <span data-ttu-id="4e25b-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4e25b-131">OUTPUTS</span></span>

### <span data-ttu-id="4e25b-132">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4e25b-132">BatchAccountContext</span></span>

## <span data-ttu-id="4e25b-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4e25b-133">NOTES</span></span>

## <span data-ttu-id="4e25b-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4e25b-134">RELATED LINKS</span></span>

[<span data-ttu-id="4e25b-135">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="4e25b-135">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="4e25b-136">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="4e25b-136">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="4e25b-137">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="4e25b-137">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="4e25b-138">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="4e25b-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
