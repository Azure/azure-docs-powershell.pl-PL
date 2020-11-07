---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/new-azurermiothubexportdevices
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
ms.openlocfilehash: 2f9122b2683721aa7f92bc1695b6c314e83d76c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718921"
---
# <span data-ttu-id="baf75-101">New-AzureRmIotHubExportDevices</span><span class="sxs-lookup"><span data-stu-id="baf75-101">New-AzureRmIotHubExportDevices</span></span>

## <span data-ttu-id="baf75-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="baf75-102">SYNOPSIS</span></span>
<span data-ttu-id="baf75-103">Umożliwia utworzenie nowego zadania eksportowania urządzeń.</span><span class="sxs-lookup"><span data-stu-id="baf75-103">Creates a new export devices job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="baf75-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="baf75-104">SYNTAX</span></span>

```
New-AzureRmIotHubExportDevices [-ResourceGroupName] <String> [-Name] <String>
 [-ExportBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="baf75-105">Opis</span><span class="sxs-lookup"><span data-stu-id="baf75-105">DESCRIPTION</span></span>
<span data-ttu-id="baf75-106">Tworzy nowe zadanie eksportu urządzeń dla IotHub.</span><span class="sxs-lookup"><span data-stu-id="baf75-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="baf75-107">Spowoduje to wyeksportowanie wszystkich urządzeń do określonego kontenera.</span><span class="sxs-lookup"><span data-stu-id="baf75-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="baf75-108">Zapoznaj się z następującym artykułem dotyczącym generowania identyfikatora URI SAS.</span><span class="sxs-lookup"><span data-stu-id="baf75-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="baf75-109"> https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span><span class="sxs-lookup"><span data-stu-id="baf75-109">https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span></span>

## <span data-ttu-id="baf75-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="baf75-110">EXAMPLES</span></span>

### <span data-ttu-id="baf75-111">Przykład 1 problem dotyczący żądania eksportowania urządzenia.</span><span class="sxs-lookup"><span data-stu-id="baf75-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzureRmIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys $true
```

<span data-ttu-id="baf75-112">Tworzy nowe żądanie eksportu urządzenia dla IotHub "myiothub" z wyłączeniem kluczy.</span><span class="sxs-lookup"><span data-stu-id="baf75-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="baf75-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="baf75-113">PARAMETERS</span></span>

### <span data-ttu-id="baf75-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baf75-114">-DefaultProfile</span></span>
<span data-ttu-id="baf75-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="baf75-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baf75-116">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="baf75-116">-ExportBlobContainerUri</span></span>
<span data-ttu-id="baf75-117">Identyfikator URI, do którego ma zostać wyeksportowany obiekt BLOB.</span><span class="sxs-lookup"><span data-stu-id="baf75-117">The Uri to export the blob to.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baf75-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="baf75-118">-Name</span></span>
<span data-ttu-id="baf75-119">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="baf75-119">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baf75-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baf75-120">-ResourceGroupName</span></span>
<span data-ttu-id="baf75-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="baf75-121">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baf75-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="baf75-122">-Confirm</span></span>
<span data-ttu-id="baf75-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="baf75-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baf75-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baf75-124">-WhatIf</span></span>
<span data-ttu-id="baf75-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="baf75-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="baf75-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="baf75-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baf75-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baf75-127">CommonParameters</span></span>
<span data-ttu-id="baf75-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baf75-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baf75-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baf75-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baf75-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="baf75-130">INPUTS</span></span>

### <span data-ttu-id="baf75-131">System. String</span><span class="sxs-lookup"><span data-stu-id="baf75-131">System.String</span></span>

## <span data-ttu-id="baf75-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="baf75-132">OUTPUTS</span></span>

### <span data-ttu-id="baf75-133">Microsoft. Azure. Management. IotHub. MODELES. JobResponse</span><span class="sxs-lookup"><span data-stu-id="baf75-133">Microsoft.Azure.Management.IotHub.Models.JobResponse</span></span>

## <span data-ttu-id="baf75-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="baf75-134">NOTES</span></span>

## <span data-ttu-id="baf75-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="baf75-135">RELATED LINKS</span></span>

