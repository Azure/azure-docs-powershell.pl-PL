---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRegistryStatistic.md
ms.openlocfilehash: d9c53652dab75b342dbf410cae8e8968534afcc9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552912"
---
# <span data-ttu-id="feeec-101">Get-AzureRmIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="feeec-101">Get-AzureRmIotHubRegistryStatistic</span></span>

## <span data-ttu-id="feeec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="feeec-102">SYNOPSIS</span></span>
<span data-ttu-id="feeec-103">Pobiera RegistryStatistics dla IotHub.</span><span class="sxs-lookup"><span data-stu-id="feeec-103">Gets the RegistryStatistics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="feeec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="feeec-104">SYNTAX</span></span>

```
Get-AzureRmIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="feeec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="feeec-105">DESCRIPTION</span></span>
<span data-ttu-id="feeec-106">Pobiera RegistryStatistics dla IotHub.</span><span class="sxs-lookup"><span data-stu-id="feeec-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="feeec-107">W tym artykule podano informacje o liczbie wszystkich urządzeń, włączonych i wyłączonych w IotHub.</span><span class="sxs-lookup"><span data-stu-id="feeec-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="feeec-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="feeec-108">EXAMPLES</span></span>

### <span data-ttu-id="feeec-109">Przykład 1 Pobierz RegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="feeec-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzureRmIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="feeec-110">Pobiera RegistryStatictics dla IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="feeec-110">Gets the RegistryStatictics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="feeec-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="feeec-111">PARAMETERS</span></span>

### <span data-ttu-id="feeec-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feeec-112">-DefaultProfile</span></span>
<span data-ttu-id="feeec-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="feeec-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feeec-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="feeec-114">-Name</span></span>
<span data-ttu-id="feeec-115">Nazwa Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="feeec-115">Name of the IoT hub.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="feeec-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="feeec-116">-ResourceGroupName</span></span>
<span data-ttu-id="feeec-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="feeec-117">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="feeec-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feeec-118">CommonParameters</span></span>
<span data-ttu-id="feeec-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="feeec-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feeec-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="feeec-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feeec-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="feeec-121">INPUTS</span></span>

### <span data-ttu-id="feeec-122">System. String</span><span class="sxs-lookup"><span data-stu-id="feeec-122">System.String</span></span>

## <span data-ttu-id="feeec-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="feeec-123">OUTPUTS</span></span>

### <span data-ttu-id="feeec-124">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. Management. IotHub. MODELES. PSIotHubRegistryStatistics, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral; PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="feeec-124">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="feeec-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="feeec-125">NOTES</span></span>

## <span data-ttu-id="feeec-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="feeec-126">RELATED LINKS</span></span>

