---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubimportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
ms.openlocfilehash: 2fb9949ecdef64423c6cc074b43f8b58a2ff9e60
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705223"
---
# <span data-ttu-id="99f81-101">New-AzIotHubImportDevice</span><span class="sxs-lookup"><span data-stu-id="99f81-101">New-AzIotHubImportDevice</span></span>

## <span data-ttu-id="99f81-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="99f81-102">SYNOPSIS</span></span>
<span data-ttu-id="99f81-103">Umożliwia utworzenie nowego zadania importu urządzeń.</span><span class="sxs-lookup"><span data-stu-id="99f81-103">Creates a new import devices job.</span></span>

## <span data-ttu-id="99f81-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="99f81-104">SYNTAX</span></span>

```
New-AzIotHubImportDevice [-ResourceGroupName] <String> [-Name] <String> [-InputBlobContainerUri] <String>
 [-OutputBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99f81-105">Opis</span><span class="sxs-lookup"><span data-stu-id="99f81-105">DESCRIPTION</span></span>
<span data-ttu-id="99f81-106">Tworzy nowe zadanie importu urządzeń dla IotHub.</span><span class="sxs-lookup"><span data-stu-id="99f81-106">Creates a new import devices job for the IotHub.</span></span>
<span data-ttu-id="99f81-107">Spowoduje to zaimportowanie wszystkich urządzeń do IotHub z określonego kontenera.</span><span class="sxs-lookup"><span data-stu-id="99f81-107">This will import all the devices to the IotHub from the specified container.</span></span> <span data-ttu-id="99f81-108">Zapoznaj się z następującym artykułem dotyczącym generowania identyfikatora URI SAS.</span><span class="sxs-lookup"><span data-stu-id="99f81-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="99f81-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="99f81-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="99f81-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="99f81-110">EXAMPLES</span></span>

### <span data-ttu-id="99f81-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="99f81-111">Example 1</span></span>
```
PS C:\> New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

<span data-ttu-id="99f81-112">Tworzy nowe żądanie importu urządzenia dla IotHub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="99f81-112">Creates a new import device request for the IotHub "myiothub".</span></span>

## <span data-ttu-id="99f81-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="99f81-113">PARAMETERS</span></span>

### <span data-ttu-id="99f81-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99f81-114">-DefaultProfile</span></span>
<span data-ttu-id="99f81-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="99f81-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99f81-116">-InputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="99f81-116">-InputBlobContainerUri</span></span>
<span data-ttu-id="99f81-117">Wejściowy identyfikator URI kontenera BLOB dla FileUpload</span><span class="sxs-lookup"><span data-stu-id="99f81-117">Input Blob Container Uri for FileUpload</span></span>

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

### <span data-ttu-id="99f81-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="99f81-118">-Name</span></span>
<span data-ttu-id="99f81-119">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="99f81-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="99f81-120">-OutputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="99f81-120">-OutputBlobContainerUri</span></span>
<span data-ttu-id="99f81-121">Identyfikator URI, do którego ma zostać napisana produkcja.</span><span class="sxs-lookup"><span data-stu-id="99f81-121">The Uri to write the output to.</span></span> 

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

### <span data-ttu-id="99f81-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99f81-122">-ResourceGroupName</span></span>
<span data-ttu-id="99f81-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="99f81-123">Resource Group Name</span></span>

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

### <span data-ttu-id="99f81-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="99f81-124">-Confirm</span></span>
<span data-ttu-id="99f81-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99f81-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99f81-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99f81-126">-WhatIf</span></span>
<span data-ttu-id="99f81-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99f81-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99f81-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="99f81-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99f81-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99f81-129">CommonParameters</span></span>
<span data-ttu-id="99f81-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99f81-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99f81-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99f81-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99f81-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99f81-132">INPUTS</span></span>

### <span data-ttu-id="99f81-133">System. String</span><span class="sxs-lookup"><span data-stu-id="99f81-133">System.String</span></span>

## <span data-ttu-id="99f81-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="99f81-134">OUTPUTS</span></span>

### <span data-ttu-id="99f81-135">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="99f81-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="99f81-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="99f81-136">NOTES</span></span>

## <span data-ttu-id="99f81-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99f81-137">RELATED LINKS</span></span>