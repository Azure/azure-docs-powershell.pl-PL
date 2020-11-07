---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRegistryStatistic.md
ms.openlocfilehash: a472ce25d648a70d9f47b6268b6bdf4f606f2a08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718860"
---
# <span data-ttu-id="625d6-101">Get-AzureRmIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="625d6-101">Get-AzureRmIotHubRegistryStatistic</span></span>

## <span data-ttu-id="625d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="625d6-102">SYNOPSIS</span></span>
<span data-ttu-id="625d6-103">Pobiera RegistryStatistics dla IotHub.</span><span class="sxs-lookup"><span data-stu-id="625d6-103">Gets the RegistryStatistics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="625d6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="625d6-104">SYNTAX</span></span>

```
Get-AzureRmIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="625d6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="625d6-105">DESCRIPTION</span></span>
<span data-ttu-id="625d6-106">Pobiera RegistryStatistics dla IotHub.</span><span class="sxs-lookup"><span data-stu-id="625d6-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="625d6-107">W tym artykule podano informacje o liczbie wszystkich urządzeń, włączonych i wyłączonych w IotHub.</span><span class="sxs-lookup"><span data-stu-id="625d6-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="625d6-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="625d6-108">EXAMPLES</span></span>

### <span data-ttu-id="625d6-109">Przykład 1 Pobierz RegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="625d6-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzureRmIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="625d6-110">Pobiera RegistryStatictics dla IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="625d6-110">Gets the RegistryStatictics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="625d6-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="625d6-111">PARAMETERS</span></span>

### <span data-ttu-id="625d6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="625d6-112">-DefaultProfile</span></span>
<span data-ttu-id="625d6-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="625d6-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="625d6-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="625d6-114">-Name</span></span>
<span data-ttu-id="625d6-115">Nazwa Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="625d6-115">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="625d6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="625d6-116">-ResourceGroupName</span></span>
<span data-ttu-id="625d6-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="625d6-117">Resource Group Name</span></span>

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

### <span data-ttu-id="625d6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="625d6-118">CommonParameters</span></span>
<span data-ttu-id="625d6-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="625d6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="625d6-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="625d6-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="625d6-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="625d6-121">INPUTS</span></span>

### <span data-ttu-id="625d6-122">System. String</span><span class="sxs-lookup"><span data-stu-id="625d6-122">System.String</span></span>

## <span data-ttu-id="625d6-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="625d6-123">OUTPUTS</span></span>

### <span data-ttu-id="625d6-124">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHubRegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="625d6-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="625d6-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="625d6-125">NOTES</span></span>

## <span data-ttu-id="625d6-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="625d6-126">RELATED LINKS</span></span>
