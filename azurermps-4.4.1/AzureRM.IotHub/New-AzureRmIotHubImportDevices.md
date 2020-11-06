---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubImportDevices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubImportDevices.md
ms.openlocfilehash: f8c2d2b7508e07dd5f42287a95623c3a6cf245de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553287"
---
# <span data-ttu-id="0d177-101">New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="0d177-101">New-AzureRmIotHubImportDevices</span></span>

## <span data-ttu-id="0d177-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0d177-102">SYNOPSIS</span></span>
<span data-ttu-id="0d177-103">Umożliwia utworzenie nowego zadania importu urządzeń.</span><span class="sxs-lookup"><span data-stu-id="0d177-103">Creates a new import devices job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d177-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0d177-104">SYNTAX</span></span>

```
New-AzureRmIotHubImportDevices [-ResourceGroupName] <String> [-Name] <String> [-InputBlobContainerUri] <String>
 [-OutputBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0d177-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0d177-105">DESCRIPTION</span></span>
<span data-ttu-id="0d177-106">Tworzy nowe zadanie importu urządzeń dla IotHub.</span><span class="sxs-lookup"><span data-stu-id="0d177-106">Creates a new import devices job for the IotHub.</span></span>
<span data-ttu-id="0d177-107">Spowoduje to zaimportowanie wszystkich urządzeń do IotHub z określonego kontenera.</span><span class="sxs-lookup"><span data-stu-id="0d177-107">This will import all the devices to the IotHub from the specified container.</span></span> <span data-ttu-id="0d177-108">Zapoznaj się z następującym artykułem dotyczącym generowania identyfikatora URI SAS.</span><span class="sxs-lookup"><span data-stu-id="0d177-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="0d177-109"> https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span><span class="sxs-lookup"><span data-stu-id="0d177-109">https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span></span>

## <span data-ttu-id="0d177-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0d177-110">EXAMPLES</span></span>

### <span data-ttu-id="0d177-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0d177-111">Example 1</span></span>
```
PS C:\> New-AzureRmIotHubImportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

<span data-ttu-id="0d177-112">Tworzy nowe żądanie importu urządzenia dla IotHub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="0d177-112">Creates a new import device request for the IotHub "myiothub".</span></span>

## <span data-ttu-id="0d177-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0d177-113">PARAMETERS</span></span>

### <span data-ttu-id="0d177-114">-InputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="0d177-114">-InputBlobContainerUri</span></span>
<span data-ttu-id="0d177-115">Wejściowy identyfikator URI kontenera BLOB dla FileUpload</span><span class="sxs-lookup"><span data-stu-id="0d177-115">Input Blob Container Uri for FileUpload</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d177-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0d177-116">-Name</span></span>
<span data-ttu-id="0d177-117">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="0d177-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="0d177-118">-OutputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="0d177-118">-OutputBlobContainerUri</span></span>
<span data-ttu-id="0d177-119">Identyfikator URI, do którego ma zostać napisana produkcja.</span><span class="sxs-lookup"><span data-stu-id="0d177-119">The Uri to write the output to.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d177-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d177-120">-ResourceGroupName</span></span>
<span data-ttu-id="0d177-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0d177-121">Resource Group Name</span></span>

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

### <span data-ttu-id="0d177-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0d177-122">-Confirm</span></span>
<span data-ttu-id="0d177-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d177-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d177-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d177-124">-WhatIf</span></span>
<span data-ttu-id="0d177-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d177-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d177-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0d177-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d177-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d177-127">-DefaultProfile</span></span>
<span data-ttu-id="0d177-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0d177-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d177-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d177-129">CommonParameters</span></span>
<span data-ttu-id="0d177-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d177-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d177-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d177-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d177-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d177-132">INPUTS</span></span>

### <span data-ttu-id="0d177-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0d177-133">System.String</span></span>

## <span data-ttu-id="0d177-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0d177-134">OUTPUTS</span></span>

### <span data-ttu-id="0d177-135">Microsoft. Azure. Management. IotHub. MODELES. JobResponse</span><span class="sxs-lookup"><span data-stu-id="0d177-135">Microsoft.Azure.Management.IotHub.Models.JobResponse</span></span>

## <span data-ttu-id="0d177-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0d177-136">NOTES</span></span>

## <span data-ttu-id="0d177-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d177-137">RELATED LINKS</span></span>

