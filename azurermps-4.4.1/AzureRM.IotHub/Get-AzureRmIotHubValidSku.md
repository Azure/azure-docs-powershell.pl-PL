---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubValidSku.md
ms.openlocfilehash: 904fb627be4460fbbca0dc6dae9a68fc0dd468ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553292"
---
# <span data-ttu-id="66f3a-101">Get-AzureRmIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="66f3a-101">Get-AzureRmIotHubValidSku</span></span>

## <span data-ttu-id="66f3a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="66f3a-102">SYNOPSIS</span></span>
<span data-ttu-id="66f3a-103">Pobiera wszystkie prawidłowe jednostki SKU, do których ta IotHub może przejść.</span><span class="sxs-lookup"><span data-stu-id="66f3a-103">Gets all valid skus that this IotHub can transition to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66f3a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="66f3a-104">SYNTAX</span></span>

```
Get-AzureRmIotHubValidSku [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66f3a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="66f3a-105">DESCRIPTION</span></span>
<span data-ttu-id="66f3a-106">Pobiera wszystkie prawidłowe jednostki SKU, do których ta IotHub może przejść.</span><span class="sxs-lookup"><span data-stu-id="66f3a-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="66f3a-107">IotHub nie może przechodzić między bezpłatnymi i płatnymi jednostkami SKU oraz odwrotnie.</span><span class="sxs-lookup"><span data-stu-id="66f3a-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="66f3a-108">Jeśli chcesz to zrobić, musisz usunąć i ponownie utworzyć iothub.</span><span class="sxs-lookup"><span data-stu-id="66f3a-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="66f3a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="66f3a-109">EXAMPLES</span></span>

### <span data-ttu-id="66f3a-110">Przykład 1 pobieranie prawidłowych wersji SKU</span><span class="sxs-lookup"><span data-stu-id="66f3a-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzureRmIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="66f3a-111">Pobiera listę wszystkich wersji SKU dla IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="66f3a-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="66f3a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="66f3a-112">PARAMETERS</span></span>

### <span data-ttu-id="66f3a-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="66f3a-113">-Name</span></span>
<span data-ttu-id="66f3a-114">Nazwa Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="66f3a-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="66f3a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66f3a-115">-ResourceGroupName</span></span>
<span data-ttu-id="66f3a-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="66f3a-116">Resource Group Name</span></span>

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

### <span data-ttu-id="66f3a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66f3a-117">-DefaultProfile</span></span>
<span data-ttu-id="66f3a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="66f3a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66f3a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66f3a-119">CommonParameters</span></span>
<span data-ttu-id="66f3a-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66f3a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66f3a-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66f3a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66f3a-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66f3a-122">INPUTS</span></span>

### <span data-ttu-id="66f3a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="66f3a-123">System.String</span></span>

## <span data-ttu-id="66f3a-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="66f3a-124">OUTPUTS</span></span>

### <span data-ttu-id="66f3a-125">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. Management. IotHub. MODELES. PSIotHubSkuDescription, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral; PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="66f3a-125">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="66f3a-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="66f3a-126">NOTES</span></span>

## <span data-ttu-id="66f3a-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="66f3a-127">RELATED LINKS</span></span>

