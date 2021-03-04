---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/new-aziothubimportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
ms.openlocfilehash: f2a2daebcb77746ae087fe527245376963fade5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956154"
---
# <span data-ttu-id="72f17-101">New-AzIotHubImportDevice</span><span class="sxs-lookup"><span data-stu-id="72f17-101">New-AzIotHubImportDevice</span></span>

## <span data-ttu-id="72f17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72f17-102">SYNOPSIS</span></span>
<span data-ttu-id="72f17-103">Tworzy nowe zadanie importowania urządzeń.</span><span class="sxs-lookup"><span data-stu-id="72f17-103">Creates a new import devices job.</span></span>

## <span data-ttu-id="72f17-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="72f17-104">SYNTAX</span></span>

```
New-AzIotHubImportDevice [-ResourceGroupName] <String> [-Name] <String> [-InputBlobContainerUri] <String>
 [-OutputBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72f17-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="72f17-105">DESCRIPTION</span></span>
<span data-ttu-id="72f17-106">Tworzy nowe zadanie importowania urządzeń dla usługi IotHub.</span><span class="sxs-lookup"><span data-stu-id="72f17-106">Creates a new import devices job for the IotHub.</span></span>
<span data-ttu-id="72f17-107">Spowoduje to zaimportowanie wszystkich urządzeń do aplikacji IotHub z określonego kontenera.</span><span class="sxs-lookup"><span data-stu-id="72f17-107">This will import all the devices to the IotHub from the specified container.</span></span> <span data-ttu-id="72f17-108">Zobacz poniższy artykuł na temat sposobu generowania URI SAS.</span><span class="sxs-lookup"><span data-stu-id="72f17-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="72f17-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="72f17-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="72f17-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="72f17-110">EXAMPLES</span></span>

### <span data-ttu-id="72f17-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="72f17-111">Example 1</span></span>
```
PS C:\> New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

<span data-ttu-id="72f17-112">Tworzy nowe żądanie importu urządzenia dla aplikacji IotHub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="72f17-112">Creates a new import device request for the IotHub "myiothub".</span></span>

## <span data-ttu-id="72f17-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72f17-113">PARAMETERS</span></span>

### <span data-ttu-id="72f17-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72f17-114">-DefaultProfile</span></span>
<span data-ttu-id="72f17-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="72f17-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72f17-116">-InputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="72f17-116">-InputBlobContainerUri</span></span>
<span data-ttu-id="72f17-117">Input Blob Container Uri for FileUpload</span><span class="sxs-lookup"><span data-stu-id="72f17-117">Input Blob Container Uri for FileUpload</span></span>

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

### <span data-ttu-id="72f17-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="72f17-118">-Name</span></span>
<span data-ttu-id="72f17-119">Nazwa aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="72f17-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="72f17-120">-OutputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="72f17-120">-OutputBlobContainerUri</span></span>
<span data-ttu-id="72f17-121">The Uri to write the output to.</span><span class="sxs-lookup"><span data-stu-id="72f17-121">The Uri to write the output to.</span></span> 

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

### <span data-ttu-id="72f17-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72f17-122">-ResourceGroupName</span></span>
<span data-ttu-id="72f17-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="72f17-123">Resource Group Name</span></span>

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

### <span data-ttu-id="72f17-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="72f17-124">-Confirm</span></span>
<span data-ttu-id="72f17-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="72f17-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72f17-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72f17-126">-WhatIf</span></span>
<span data-ttu-id="72f17-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72f17-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72f17-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="72f17-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72f17-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72f17-129">CommonParameters</span></span>
<span data-ttu-id="72f17-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72f17-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72f17-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72f17-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72f17-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72f17-132">INPUTS</span></span>

### <span data-ttu-id="72f17-133">System.String</span><span class="sxs-lookup"><span data-stu-id="72f17-133">System.String</span></span>

## <span data-ttu-id="72f17-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72f17-134">OUTPUTS</span></span>

### <span data-ttu-id="72f17-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="72f17-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="72f17-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="72f17-136">NOTES</span></span>

## <span data-ttu-id="72f17-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72f17-137">RELATED LINKS</span></span>
