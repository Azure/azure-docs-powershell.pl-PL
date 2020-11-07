---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubJob.md
ms.openlocfilehash: 36c336f516cf2621a64a6e0e353e93e7defa03b1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891389"
---
# <span data-ttu-id="016f9-101">Get-AzIotHubJob</span><span class="sxs-lookup"><span data-stu-id="016f9-101">Get-AzIotHubJob</span></span>

## <span data-ttu-id="016f9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="016f9-102">SYNOPSIS</span></span>
<span data-ttu-id="016f9-103">Pobiera informacje o zadaniu programu IotHub.</span><span class="sxs-lookup"><span data-stu-id="016f9-103">Gets the information about an IotHub job.</span></span>

## <span data-ttu-id="016f9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="016f9-104">SYNTAX</span></span>

```
Get-AzIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="016f9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="016f9-105">DESCRIPTION</span></span>
<span data-ttu-id="016f9-106">Pobiera informacje o zadaniu programu IotHub.</span><span class="sxs-lookup"><span data-stu-id="016f9-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="016f9-107">Zadanie programu IotHub zostanie utworzone po zainicjowaniu operacji importu lub eksportu przy użyciu poleceń New-AzIotHubExportDevices lub New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="016f9-107">An IotHub Job gets created when an import or export operation is initialized using the New-AzIotHubExportDevices or New-AzIotHubImportDevices commands.</span></span>
<span data-ttu-id="016f9-108">Możesz wyświetlić wszystkie zadania lub filtrować zadania według identyfikatora zadania.</span><span class="sxs-lookup"><span data-stu-id="016f9-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="016f9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="016f9-109">EXAMPLES</span></span>

### <span data-ttu-id="016f9-110">Przykład 1 Lista wszystkich zadań</span><span class="sxs-lookup"><span data-stu-id="016f9-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="016f9-111">Pobiera wszystkie zadania dla IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="016f9-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="016f9-112">Przykład 2 uzyskiwanie określonego zadania</span><span class="sxs-lookup"><span data-stu-id="016f9-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="016f9-113">Pobiera informacje o zadaniu o identyfikatorze "3630fc31-4caa-43e8-a232-ea0577221cb2" dla IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="016f9-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="016f9-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="016f9-114">PARAMETERS</span></span>

### <span data-ttu-id="016f9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="016f9-115">-DefaultProfile</span></span>
<span data-ttu-id="016f9-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="016f9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="016f9-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="016f9-117">-JobId</span></span>
<span data-ttu-id="016f9-118">Identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="016f9-118">The Job Identifier.</span></span> 

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

### <span data-ttu-id="016f9-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="016f9-119">-Name</span></span>
<span data-ttu-id="016f9-120">Nazwa Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="016f9-120">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="016f9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="016f9-121">-ResourceGroupName</span></span>
<span data-ttu-id="016f9-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="016f9-122">Resource Group Name</span></span>

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

### <span data-ttu-id="016f9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="016f9-123">CommonParameters</span></span>
<span data-ttu-id="016f9-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="016f9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="016f9-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="016f9-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="016f9-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="016f9-126">INPUTS</span></span>

### <span data-ttu-id="016f9-127">System. String</span><span class="sxs-lookup"><span data-stu-id="016f9-127">System.String</span></span>

## <span data-ttu-id="016f9-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="016f9-128">OUTPUTS</span></span>

### <span data-ttu-id="016f9-129">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="016f9-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="016f9-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="016f9-130">NOTES</span></span>

## <span data-ttu-id="016f9-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="016f9-131">RELATED LINKS</span></span>
