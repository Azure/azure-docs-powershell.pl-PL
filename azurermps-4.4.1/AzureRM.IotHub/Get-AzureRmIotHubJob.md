---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
ms.openlocfilehash: b0ea6f3cae3fe978a3d24b055eb47693ea466272
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718196"
---
# <span data-ttu-id="a1e15-101">Get-AzureRmIotHubJob</span><span class="sxs-lookup"><span data-stu-id="a1e15-101">Get-AzureRmIotHubJob</span></span>

## <span data-ttu-id="a1e15-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a1e15-102">SYNOPSIS</span></span>
<span data-ttu-id="a1e15-103">Pobiera informacje o zadaniu programu IotHub.</span><span class="sxs-lookup"><span data-stu-id="a1e15-103">Gets the information about an IotHub job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1e15-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a1e15-104">SYNTAX</span></span>

```
Get-AzureRmIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1e15-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a1e15-105">DESCRIPTION</span></span>
<span data-ttu-id="a1e15-106">Pobiera informacje o zadaniu programu IotHub.</span><span class="sxs-lookup"><span data-stu-id="a1e15-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="a1e15-107">Zadanie programu IotHub zostanie utworzone, gdy operacja importu lub eksportu jest initialted przy użyciu poleceń New-AzureRmIotHubExportDevices lub New-AzureRmIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="a1e15-107">An IotHub Job gets created when an import or export operation is initialted using the New-AzureRmIotHubExportDevices or New-AzureRmIotHubImportDevices commands.</span></span>
<span data-ttu-id="a1e15-108">Możesz wyświetlić wszystkie zadania lub filtrować zadania według identyfikatora zadania.</span><span class="sxs-lookup"><span data-stu-id="a1e15-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="a1e15-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a1e15-109">EXAMPLES</span></span>

### <span data-ttu-id="a1e15-110">Przykład 1 Lista wszystkich zadań</span><span class="sxs-lookup"><span data-stu-id="a1e15-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="a1e15-111">Pobiera wszystkie zadania dla IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="a1e15-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="a1e15-112">Przykład 2 uzyskiwanie określonego zadania</span><span class="sxs-lookup"><span data-stu-id="a1e15-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="a1e15-113">Pobiera informacje o zadaniu o identyfikatorze "3630fc31-4caa-43e8-a232-ea0577221cb2" dla IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="a1e15-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="a1e15-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a1e15-114">PARAMETERS</span></span>

### <span data-ttu-id="a1e15-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="a1e15-115">-JobId</span></span>
<span data-ttu-id="a1e15-116">Identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="a1e15-116">The Job Identifier.</span></span> 

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

### <span data-ttu-id="a1e15-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a1e15-117">-Name</span></span>
<span data-ttu-id="a1e15-118">Nazwa Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="a1e15-118">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="a1e15-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1e15-119">-ResourceGroupName</span></span>
<span data-ttu-id="a1e15-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a1e15-120">Resource Group Name</span></span>

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

### <span data-ttu-id="a1e15-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1e15-121">-DefaultProfile</span></span>
<span data-ttu-id="a1e15-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1e15-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1e15-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1e15-123">CommonParameters</span></span>
<span data-ttu-id="a1e15-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1e15-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1e15-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1e15-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1e15-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1e15-126">INPUTS</span></span>

### <span data-ttu-id="a1e15-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a1e15-127">System.String</span></span>

## <span data-ttu-id="a1e15-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a1e15-128">OUTPUTS</span></span>

### <span data-ttu-id="a1e15-129">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="a1e15-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>
<span data-ttu-id="a1e15-130">System. Collections. Generic. list \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. MODELES. PSIotHubJobResponse, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral; PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="a1e15-130">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="a1e15-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a1e15-131">NOTES</span></span>

## <span data-ttu-id="a1e15-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1e15-132">RELATED LINKS</span></span>

