---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
ms.openlocfilehash: 684b892d2c2cc995e12ae6327541f13428da270f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718866"
---
# <span data-ttu-id="2deef-101">Get-AzureRmIotHubJob</span><span class="sxs-lookup"><span data-stu-id="2deef-101">Get-AzureRmIotHubJob</span></span>

## <span data-ttu-id="2deef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2deef-102">SYNOPSIS</span></span>
<span data-ttu-id="2deef-103">Pobiera informacje o zadaniu programu IotHub.</span><span class="sxs-lookup"><span data-stu-id="2deef-103">Gets the information about an IotHub job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2deef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2deef-104">SYNTAX</span></span>

```
Get-AzureRmIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2deef-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2deef-105">DESCRIPTION</span></span>
<span data-ttu-id="2deef-106">Pobiera informacje o zadaniu programu IotHub.</span><span class="sxs-lookup"><span data-stu-id="2deef-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="2deef-107">Zadanie programu IotHub zostanie utworzone, gdy operacja importu lub eksportu jest initialted przy użyciu poleceń New-AzureRmIotHubExportDevices lub New-AzureRmIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="2deef-107">An IotHub Job gets created when an import or export operation is initialted using the New-AzureRmIotHubExportDevices or New-AzureRmIotHubImportDevices commands.</span></span>
<span data-ttu-id="2deef-108">Możesz wyświetlić wszystkie zadania lub filtrować zadania według identyfikatora zadania.</span><span class="sxs-lookup"><span data-stu-id="2deef-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="2deef-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2deef-109">EXAMPLES</span></span>

### <span data-ttu-id="2deef-110">Przykład 1 Lista wszystkich zadań</span><span class="sxs-lookup"><span data-stu-id="2deef-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="2deef-111">Pobiera wszystkie zadania dla IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="2deef-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="2deef-112">Przykład 2 uzyskiwanie określonego zadania</span><span class="sxs-lookup"><span data-stu-id="2deef-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="2deef-113">Pobiera informacje o zadaniu o identyfikatorze "3630fc31-4caa-43e8-a232-ea0577221cb2" dla IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="2deef-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="2deef-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2deef-114">PARAMETERS</span></span>

### <span data-ttu-id="2deef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2deef-115">-DefaultProfile</span></span>
<span data-ttu-id="2deef-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2deef-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2deef-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="2deef-117">-JobId</span></span>
<span data-ttu-id="2deef-118">Identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="2deef-118">The Job Identifier.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2deef-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2deef-119">-Name</span></span>
<span data-ttu-id="2deef-120">Nazwa Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="2deef-120">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="2deef-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2deef-121">-ResourceGroupName</span></span>
<span data-ttu-id="2deef-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="2deef-122">Resource Group Name</span></span>

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

### <span data-ttu-id="2deef-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2deef-123">CommonParameters</span></span>
<span data-ttu-id="2deef-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2deef-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2deef-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2deef-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2deef-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2deef-126">INPUTS</span></span>

### <span data-ttu-id="2deef-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2deef-127">System.String</span></span>

## <span data-ttu-id="2deef-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2deef-128">OUTPUTS</span></span>

### <span data-ttu-id="2deef-129">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="2deef-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="2deef-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2deef-130">NOTES</span></span>

## <span data-ttu-id="2deef-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2deef-131">RELATED LINKS</span></span>
