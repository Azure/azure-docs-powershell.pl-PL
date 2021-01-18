---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
ms.openlocfilehash: 7c5c09f2379eb1c0306b89018732336b4223f5c9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503415"
---
# <span data-ttu-id="5aafc-101">Get-AzIotHubJob</span><span class="sxs-lookup"><span data-stu-id="5aafc-101">Get-AzIotHubJob</span></span>

## <span data-ttu-id="5aafc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5aafc-102">SYNOPSIS</span></span>
<span data-ttu-id="5aafc-103">Pobiera informacje o zadaniu programu IotHub.</span><span class="sxs-lookup"><span data-stu-id="5aafc-103">Gets the information about an IotHub job.</span></span>

## <span data-ttu-id="5aafc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5aafc-104">SYNTAX</span></span>

```
Get-AzIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5aafc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5aafc-105">DESCRIPTION</span></span>
<span data-ttu-id="5aafc-106">Pobiera informacje o zadaniu programu IotHub.</span><span class="sxs-lookup"><span data-stu-id="5aafc-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="5aafc-107">Zadanie programu IotHub zostanie utworzone po zainicjowaniu operacji importu lub eksportu przy użyciu poleceń New-AzIotHubExportDevices lub New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="5aafc-107">An IotHub Job gets created when an import or export operation is initialized using the New-AzIotHubExportDevices or New-AzIotHubImportDevices commands.</span></span>
<span data-ttu-id="5aafc-108">Możesz wyświetlić wszystkie zadania lub filtrować zadania według identyfikatora zadania.</span><span class="sxs-lookup"><span data-stu-id="5aafc-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="5aafc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5aafc-109">EXAMPLES</span></span>

### <span data-ttu-id="5aafc-110">Przykład 1 Lista wszystkich zadań</span><span class="sxs-lookup"><span data-stu-id="5aafc-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="5aafc-111">Pobiera wszystkie zadania dla IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="5aafc-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="5aafc-112">Przykład 2 uzyskiwanie określonego zadania</span><span class="sxs-lookup"><span data-stu-id="5aafc-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="5aafc-113">Pobiera informacje o zadaniu o identyfikatorze "3630fc31-4caa-43e8-a232-ea0577221cb2" dla IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="5aafc-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="5aafc-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5aafc-114">PARAMETERS</span></span>

### <span data-ttu-id="5aafc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aafc-115">-DefaultProfile</span></span>
<span data-ttu-id="5aafc-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5aafc-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5aafc-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="5aafc-117">-JobId</span></span>
<span data-ttu-id="5aafc-118">Identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="5aafc-118">The Job Identifier.</span></span> 

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

### <span data-ttu-id="5aafc-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5aafc-119">-Name</span></span>
<span data-ttu-id="5aafc-120">Nazwa Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="5aafc-120">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="5aafc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5aafc-121">-ResourceGroupName</span></span>
<span data-ttu-id="5aafc-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5aafc-122">Resource Group Name</span></span>

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

### <span data-ttu-id="5aafc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aafc-123">CommonParameters</span></span>
<span data-ttu-id="5aafc-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5aafc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aafc-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5aafc-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aafc-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5aafc-126">INPUTS</span></span>

### <span data-ttu-id="5aafc-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5aafc-127">System.String</span></span>

## <span data-ttu-id="5aafc-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5aafc-128">OUTPUTS</span></span>

### <span data-ttu-id="5aafc-129">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="5aafc-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="5aafc-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5aafc-130">NOTES</span></span>

## <span data-ttu-id="5aafc-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5aafc-131">RELATED LINKS</span></span>
