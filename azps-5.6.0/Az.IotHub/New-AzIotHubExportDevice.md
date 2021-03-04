---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/new-aziothubexportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
ms.openlocfilehash: 030c97a05d7f87ffc75c284250e8b67e8d3dc1fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954602"
---
# <span data-ttu-id="ba9e6-101">New-AzIotHubExportDevice</span><span class="sxs-lookup"><span data-stu-id="ba9e6-101">New-AzIotHubExportDevice</span></span>

## <span data-ttu-id="ba9e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba9e6-102">SYNOPSIS</span></span>
<span data-ttu-id="ba9e6-103">Tworzy nowe zadanie eksportowania urządzeń.</span><span class="sxs-lookup"><span data-stu-id="ba9e6-103">Creates a new export devices job.</span></span>

## <span data-ttu-id="ba9e6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ba9e6-104">SYNTAX</span></span>

```
New-AzIotHubExportDevice [-ResourceGroupName] <String> [-Name] <String> [-ExportBlobContainerUri] <String>
 [-ExcludeKeys] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba9e6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ba9e6-105">DESCRIPTION</span></span>
<span data-ttu-id="ba9e6-106">Tworzy nowe zadanie eksportowania urządzeń dla usługi IotHub.</span><span class="sxs-lookup"><span data-stu-id="ba9e6-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="ba9e6-107">Spowoduje to wyeksportowanie wszystkich urządzeń do określonego kontenera.</span><span class="sxs-lookup"><span data-stu-id="ba9e6-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="ba9e6-108">Zobacz poniższy artykuł na temat sposobu generowania URI SAS.</span><span class="sxs-lookup"><span data-stu-id="ba9e6-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="ba9e6-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="ba9e6-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="ba9e6-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ba9e6-110">EXAMPLES</span></span>

### <span data-ttu-id="ba9e6-111">Przykład 1. Problem z żądaniem urządzenia eksportu.</span><span class="sxs-lookup"><span data-stu-id="ba9e6-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

<span data-ttu-id="ba9e6-112">Tworzy nowe żądanie urządzenia eksportu dla aplikacji IotHub "myiothub" z wyjątkiem kluczy.</span><span class="sxs-lookup"><span data-stu-id="ba9e6-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="ba9e6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba9e6-113">PARAMETERS</span></span>

### <span data-ttu-id="ba9e6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba9e6-114">-DefaultProfile</span></span>
<span data-ttu-id="ba9e6-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ba9e6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba9e6-116">- ExcludeKeys</span><span class="sxs-lookup"><span data-stu-id="ba9e6-116">-ExcludeKeys</span></span>
<span data-ttu-id="ba9e6-117">Umożliwia eksportowanie urządzeń bez kluczy.</span><span class="sxs-lookup"><span data-stu-id="ba9e6-117">Allows to export devices without keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba9e6-118">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="ba9e6-118">-ExportBlobContainerUri</span></span>
<span data-ttu-id="ba9e6-119">The Uri to export the blob to.</span><span class="sxs-lookup"><span data-stu-id="ba9e6-119">The Uri to export the blob to.</span></span> 

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

### <span data-ttu-id="ba9e6-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ba9e6-120">-Name</span></span>
<span data-ttu-id="ba9e6-121">Nazwa aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="ba9e6-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="ba9e6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba9e6-122">-ResourceGroupName</span></span>
<span data-ttu-id="ba9e6-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ba9e6-123">Resource Group Name</span></span>

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

### <span data-ttu-id="ba9e6-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ba9e6-124">-Confirm</span></span>
<span data-ttu-id="ba9e6-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ba9e6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba9e6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba9e6-126">-WhatIf</span></span>
<span data-ttu-id="ba9e6-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba9e6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba9e6-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ba9e6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba9e6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba9e6-129">CommonParameters</span></span>
<span data-ttu-id="ba9e6-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba9e6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba9e6-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba9e6-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba9e6-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba9e6-132">INPUTS</span></span>

### <span data-ttu-id="ba9e6-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ba9e6-133">System.String</span></span>

## <span data-ttu-id="ba9e6-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba9e6-134">OUTPUTS</span></span>

### <span data-ttu-id="ba9e6-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="ba9e6-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="ba9e6-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ba9e6-136">NOTES</span></span>

## <span data-ttu-id="ba9e6-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba9e6-137">RELATED LINKS</span></span>
