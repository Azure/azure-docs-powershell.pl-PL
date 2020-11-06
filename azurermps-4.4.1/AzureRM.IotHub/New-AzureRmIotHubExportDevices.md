---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
ms.openlocfilehash: 3191f4e451ec010a3918130142d08da6f08b3990
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553291"
---
# <span data-ttu-id="9b6b4-101">New-AzureRmIotHubExportDevices</span><span class="sxs-lookup"><span data-stu-id="9b6b4-101">New-AzureRmIotHubExportDevices</span></span>

## <span data-ttu-id="9b6b4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9b6b4-102">SYNOPSIS</span></span>
<span data-ttu-id="9b6b4-103">Umożliwia utworzenie nowego zadania eksportowania urządzeń.</span><span class="sxs-lookup"><span data-stu-id="9b6b4-103">Creates a new export devices job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b6b4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9b6b4-104">SYNTAX</span></span>

```
New-AzureRmIotHubExportDevices [-ResourceGroupName] <String> [-Name] <String>
 [-ExportBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b6b4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9b6b4-105">DESCRIPTION</span></span>
<span data-ttu-id="9b6b4-106">Tworzy nowe zadanie eksportu urządzeń dla IotHub.</span><span class="sxs-lookup"><span data-stu-id="9b6b4-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="9b6b4-107">Spowoduje to wyeksportowanie wszystkich urządzeń do określonego kontenera.</span><span class="sxs-lookup"><span data-stu-id="9b6b4-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="9b6b4-108">Zapoznaj się z następującym artykułem dotyczącym generowania identyfikatora URI SAS.</span><span class="sxs-lookup"><span data-stu-id="9b6b4-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="9b6b4-109"> https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span><span class="sxs-lookup"><span data-stu-id="9b6b4-109">https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span></span>

## <span data-ttu-id="9b6b4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9b6b4-110">EXAMPLES</span></span>

### <span data-ttu-id="9b6b4-111">Przykład 1 problem dotyczący żądania eksportowania urządzenia.</span><span class="sxs-lookup"><span data-stu-id="9b6b4-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzureRmIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys $true
```

<span data-ttu-id="9b6b4-112">Tworzy nowe żądanie eksportu urządzenia dla IotHub "myiothub" z wyłączeniem kluczy.</span><span class="sxs-lookup"><span data-stu-id="9b6b4-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="9b6b4-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9b6b4-113">PARAMETERS</span></span>

### <span data-ttu-id="9b6b4-114">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="9b6b4-114">-ExportBlobContainerUri</span></span>
<span data-ttu-id="9b6b4-115">Identyfikator URI, do którego ma zostać wyeksportowany obiekt BLOB.</span><span class="sxs-lookup"><span data-stu-id="9b6b4-115">The Uri to export the blob to.</span></span> 

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

### <span data-ttu-id="9b6b4-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9b6b4-116">-Name</span></span>
<span data-ttu-id="9b6b4-117">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="9b6b4-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="9b6b4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b6b4-118">-ResourceGroupName</span></span>
<span data-ttu-id="9b6b4-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9b6b4-119">Resource Group Name</span></span>

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

### <span data-ttu-id="9b6b4-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9b6b4-120">-Confirm</span></span>
<span data-ttu-id="9b6b4-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b6b4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b6b4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b6b4-122">-WhatIf</span></span>
<span data-ttu-id="9b6b4-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b6b4-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b6b4-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9b6b4-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b6b4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b6b4-125">-DefaultProfile</span></span>
<span data-ttu-id="9b6b4-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b6b4-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b6b4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b6b4-127">CommonParameters</span></span>
<span data-ttu-id="9b6b4-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b6b4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b6b4-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b6b4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b6b4-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b6b4-130">INPUTS</span></span>

### <span data-ttu-id="9b6b4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9b6b4-131">System.String</span></span>

## <span data-ttu-id="9b6b4-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9b6b4-132">OUTPUTS</span></span>

### <span data-ttu-id="9b6b4-133">Microsoft. Azure. Management. IotHub. MODELES. JobResponse</span><span class="sxs-lookup"><span data-stu-id="9b6b4-133">Microsoft.Azure.Management.IotHub.Models.JobResponse</span></span>

## <span data-ttu-id="9b6b4-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9b6b4-134">NOTES</span></span>

## <span data-ttu-id="9b6b4-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b6b4-135">RELATED LINKS</span></span>

