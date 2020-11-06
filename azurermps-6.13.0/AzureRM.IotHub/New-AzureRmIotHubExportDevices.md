---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/new-azurermiothubexportdevices
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
ms.openlocfilehash: 4c13a6366f0ccae803e8020f16bf2b566bd70934
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546592"
---
# <span data-ttu-id="21d9e-101">New-AzureRmIotHubExportDevices</span><span class="sxs-lookup"><span data-stu-id="21d9e-101">New-AzureRmIotHubExportDevices</span></span>

## <span data-ttu-id="21d9e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21d9e-102">SYNOPSIS</span></span>
<span data-ttu-id="21d9e-103">Umożliwia utworzenie nowego zadania eksportowania urządzeń.</span><span class="sxs-lookup"><span data-stu-id="21d9e-103">Creates a new export devices job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21d9e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21d9e-104">SYNTAX</span></span>

```
New-AzureRmIotHubExportDevices [-ResourceGroupName] <String> [-Name] <String>
 [-ExportBlobContainerUri] <String> [-ExcludeKeys] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21d9e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="21d9e-105">DESCRIPTION</span></span>
<span data-ttu-id="21d9e-106">Tworzy nowe zadanie eksportu urządzeń dla IotHub.</span><span class="sxs-lookup"><span data-stu-id="21d9e-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="21d9e-107">Spowoduje to wyeksportowanie wszystkich urządzeń do określonego kontenera.</span><span class="sxs-lookup"><span data-stu-id="21d9e-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="21d9e-108">Zapoznaj się z następującym artykułem dotyczącym generowania identyfikatora URI SAS.</span><span class="sxs-lookup"><span data-stu-id="21d9e-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="21d9e-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="21d9e-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="21d9e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21d9e-110">EXAMPLES</span></span>

### <span data-ttu-id="21d9e-111">Przykład 1 problem dotyczący żądania eksportowania urządzenia.</span><span class="sxs-lookup"><span data-stu-id="21d9e-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzureRmIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

<span data-ttu-id="21d9e-112">Tworzy nowe żądanie eksportu urządzenia dla IotHub "myiothub" z wyłączeniem kluczy.</span><span class="sxs-lookup"><span data-stu-id="21d9e-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="21d9e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21d9e-113">PARAMETERS</span></span>

### <span data-ttu-id="21d9e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21d9e-114">-DefaultProfile</span></span>
<span data-ttu-id="21d9e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="21d9e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21d9e-116">-ExcludeKeys</span><span class="sxs-lookup"><span data-stu-id="21d9e-116">-ExcludeKeys</span></span>
<span data-ttu-id="21d9e-117">Umożliwia eksportowanie urządzeń bez kluczy.</span><span class="sxs-lookup"><span data-stu-id="21d9e-117">Allows to export devices without keys.</span></span>

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

### <span data-ttu-id="21d9e-118">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="21d9e-118">-ExportBlobContainerUri</span></span>
<span data-ttu-id="21d9e-119">Identyfikator URI, do którego ma zostać wyeksportowany obiekt BLOB.</span><span class="sxs-lookup"><span data-stu-id="21d9e-119">The Uri to export the blob to.</span></span> 

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

### <span data-ttu-id="21d9e-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="21d9e-120">-Name</span></span>
<span data-ttu-id="21d9e-121">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="21d9e-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="21d9e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21d9e-122">-ResourceGroupName</span></span>
<span data-ttu-id="21d9e-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="21d9e-123">Resource Group Name</span></span>

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

### <span data-ttu-id="21d9e-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="21d9e-124">-Confirm</span></span>
<span data-ttu-id="21d9e-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21d9e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21d9e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21d9e-126">-WhatIf</span></span>
<span data-ttu-id="21d9e-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21d9e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21d9e-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="21d9e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21d9e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21d9e-129">CommonParameters</span></span>
<span data-ttu-id="21d9e-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21d9e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21d9e-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21d9e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21d9e-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21d9e-132">INPUTS</span></span>

### <span data-ttu-id="21d9e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="21d9e-133">System.String</span></span>

## <span data-ttu-id="21d9e-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21d9e-134">OUTPUTS</span></span>

### <span data-ttu-id="21d9e-135">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="21d9e-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="21d9e-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21d9e-136">NOTES</span></span>

## <span data-ttu-id="21d9e-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21d9e-137">RELATED LINKS</span></span>
