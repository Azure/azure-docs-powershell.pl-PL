---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubimportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
ms.openlocfilehash: bb1b5579869c7142bcf6cbe168ff10aaa9b7e083
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180530"
---
# <span data-ttu-id="a63a8-101">New-AzIotHubImportDevice</span><span class="sxs-lookup"><span data-stu-id="a63a8-101">New-AzIotHubImportDevice</span></span>

## <span data-ttu-id="a63a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a63a8-102">SYNOPSIS</span></span>
<span data-ttu-id="a63a8-103">Tworzy nowe zadanie importowania urządzeń.</span><span class="sxs-lookup"><span data-stu-id="a63a8-103">Creates a new import devices job.</span></span>

## <span data-ttu-id="a63a8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a63a8-104">SYNTAX</span></span>

```
New-AzIotHubImportDevice [-ResourceGroupName] <String> [-Name] <String> [-InputBlobContainerUri] <String>
 [-OutputBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a63a8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a63a8-105">DESCRIPTION</span></span>
<span data-ttu-id="a63a8-106">Tworzy nowe zadanie importowania urządzeń dla usługi IotHub.</span><span class="sxs-lookup"><span data-stu-id="a63a8-106">Creates a new import devices job for the IotHub.</span></span>
<span data-ttu-id="a63a8-107">Spowoduje to zaimportowanie wszystkich urządzeń do aplikacji IotHub z określonego kontenera.</span><span class="sxs-lookup"><span data-stu-id="a63a8-107">This will import all the devices to the IotHub from the specified container.</span></span> <span data-ttu-id="a63a8-108">Zobacz poniższy artykuł na temat sposobu generowania URI SAS.</span><span class="sxs-lookup"><span data-stu-id="a63a8-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="a63a8-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="a63a8-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="a63a8-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a63a8-110">EXAMPLES</span></span>

### <span data-ttu-id="a63a8-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a63a8-111">Example 1</span></span>
```
PS C:\> New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

<span data-ttu-id="a63a8-112">Tworzy nowe żądanie urządzenia importu dla aplikacji IotHub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="a63a8-112">Creates a new import device request for the IotHub "myiothub".</span></span>

## <span data-ttu-id="a63a8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a63a8-113">PARAMETERS</span></span>

### <span data-ttu-id="a63a8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a63a8-114">-DefaultProfile</span></span>
<span data-ttu-id="a63a8-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a63a8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a63a8-116">-InputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="a63a8-116">-InputBlobContainerUri</span></span>
<span data-ttu-id="a63a8-117">Input Blob Container Uri for FileUpload</span><span class="sxs-lookup"><span data-stu-id="a63a8-117">Input Blob Container Uri for FileUpload</span></span>

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

### <span data-ttu-id="a63a8-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a63a8-118">-Name</span></span>
<span data-ttu-id="a63a8-119">Nazwa aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="a63a8-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="a63a8-120">-OutputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="a63a8-120">-OutputBlobContainerUri</span></span>
<span data-ttu-id="a63a8-121">The Uri to write the output to.</span><span class="sxs-lookup"><span data-stu-id="a63a8-121">The Uri to write the output to.</span></span> 

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

### <span data-ttu-id="a63a8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a63a8-122">-ResourceGroupName</span></span>
<span data-ttu-id="a63a8-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a63a8-123">Resource Group Name</span></span>

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

### <span data-ttu-id="a63a8-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a63a8-124">-Confirm</span></span>
<span data-ttu-id="a63a8-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a63a8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a63a8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a63a8-126">-WhatIf</span></span>
<span data-ttu-id="a63a8-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a63a8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a63a8-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a63a8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a63a8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a63a8-129">CommonParameters</span></span>
<span data-ttu-id="a63a8-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a63a8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a63a8-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a63a8-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a63a8-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a63a8-132">INPUTS</span></span>

### <span data-ttu-id="a63a8-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a63a8-133">System.String</span></span>

## <span data-ttu-id="a63a8-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a63a8-134">OUTPUTS</span></span>

### <span data-ttu-id="a63a8-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="a63a8-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="a63a8-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a63a8-136">NOTES</span></span>

## <span data-ttu-id="a63a8-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a63a8-137">RELATED LINKS</span></span>
