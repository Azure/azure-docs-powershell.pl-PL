---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
ms.openlocfilehash: 36d59745b19df716735ce5b9b248c0ca71b7d687
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221708"
---
# <span data-ttu-id="0e060-101">Get-AzIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="0e060-101">Get-AzIotHubRegistryStatistic</span></span>

## <span data-ttu-id="0e060-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0e060-102">SYNOPSIS</span></span>
<span data-ttu-id="0e060-103">Pobiera RegistryStatistics dla IotHub.</span><span class="sxs-lookup"><span data-stu-id="0e060-103">Gets the RegistryStatistics for an IotHub.</span></span>

## <span data-ttu-id="0e060-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0e060-104">SYNTAX</span></span>

```
Get-AzIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e060-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0e060-105">DESCRIPTION</span></span>
<span data-ttu-id="0e060-106">Pobiera RegistryStatistics dla IotHub.</span><span class="sxs-lookup"><span data-stu-id="0e060-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="0e060-107">W tym artykule podano informacje o liczbie wszystkich urządzeń, włączonych i wyłączonych w IotHub.</span><span class="sxs-lookup"><span data-stu-id="0e060-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="0e060-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0e060-108">EXAMPLES</span></span>

### <span data-ttu-id="0e060-109">Przykład 1 Pobierz RegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="0e060-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="0e060-110">Pobiera RegistryStatistics dla IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="0e060-110">Gets the RegistryStatistics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="0e060-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0e060-111">PARAMETERS</span></span>

### <span data-ttu-id="0e060-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e060-112">-DefaultProfile</span></span>
<span data-ttu-id="0e060-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0e060-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e060-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0e060-114">-Name</span></span>
<span data-ttu-id="0e060-115">Nazwa Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="0e060-115">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="0e060-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e060-116">-ResourceGroupName</span></span>
<span data-ttu-id="0e060-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0e060-117">Resource Group Name</span></span>

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

### <span data-ttu-id="0e060-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e060-118">CommonParameters</span></span>
<span data-ttu-id="0e060-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e060-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e060-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e060-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e060-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e060-121">INPUTS</span></span>

### <span data-ttu-id="0e060-122">System. String</span><span class="sxs-lookup"><span data-stu-id="0e060-122">System.String</span></span>

## <span data-ttu-id="0e060-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0e060-123">OUTPUTS</span></span>

### <span data-ttu-id="0e060-124">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHubRegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="0e060-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="0e060-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0e060-125">NOTES</span></span>

## <span data-ttu-id="0e060-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e060-126">RELATED LINKS</span></span>
