---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
ms.openlocfilehash: 36d59745b19df716735ce5b9b248c0ca71b7d687
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185642"
---
# <span data-ttu-id="14e83-101">Get-AzIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="14e83-101">Get-AzIotHubRegistryStatistic</span></span>

## <span data-ttu-id="14e83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14e83-102">SYNOPSIS</span></span>
<span data-ttu-id="14e83-103">Pobiera statystykę rejestru dla aplikacji IotHub.</span><span class="sxs-lookup"><span data-stu-id="14e83-103">Gets the RegistryStatistics for an IotHub.</span></span>

## <span data-ttu-id="14e83-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="14e83-104">SYNTAX</span></span>

```
Get-AzIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14e83-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="14e83-105">DESCRIPTION</span></span>
<span data-ttu-id="14e83-106">Pobiera statystykę rejestru dla aplikacji IotHub.</span><span class="sxs-lookup"><span data-stu-id="14e83-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="14e83-107">Informacje na temat łącznej liczby urządzeń włączonych i wyłączonych w aplikacji IotHub.</span><span class="sxs-lookup"><span data-stu-id="14e83-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="14e83-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="14e83-108">EXAMPLES</span></span>

### <span data-ttu-id="14e83-109">Przykład 1. Uzyskiwanie statystyki rejestru</span><span class="sxs-lookup"><span data-stu-id="14e83-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="14e83-110">Pobiera statystykę rejestru dla usługi IotHub o nazwie "myiothub"</span><span class="sxs-lookup"><span data-stu-id="14e83-110">Gets the RegistryStatistics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="14e83-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14e83-111">PARAMETERS</span></span>

### <span data-ttu-id="14e83-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14e83-112">-DefaultProfile</span></span>
<span data-ttu-id="14e83-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="14e83-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14e83-114">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="14e83-114">-Name</span></span>
<span data-ttu-id="14e83-115">Nazwa centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="14e83-115">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="14e83-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14e83-116">-ResourceGroupName</span></span>
<span data-ttu-id="14e83-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="14e83-117">Resource Group Name</span></span>

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

### <span data-ttu-id="14e83-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14e83-118">CommonParameters</span></span>
<span data-ttu-id="14e83-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14e83-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14e83-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14e83-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14e83-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14e83-121">INPUTS</span></span>

### <span data-ttu-id="14e83-122">System.String</span><span class="sxs-lookup"><span data-stu-id="14e83-122">System.String</span></span>

## <span data-ttu-id="14e83-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14e83-123">OUTPUTS</span></span>

### <span data-ttu-id="14e83-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="14e83-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="14e83-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="14e83-125">NOTES</span></span>

## <span data-ttu-id="14e83-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14e83-126">RELATED LINKS</span></span>
