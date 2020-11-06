---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: ec5ba90fd0c3dbdbf96ddf2370948de090306611
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552611"
---
# <span data-ttu-id="af140-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="af140-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="af140-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="af140-102">SYNOPSIS</span></span>
<span data-ttu-id="af140-103">Pobiera mapowania klasyfikacji magazynu ASR.</span><span class="sxs-lookup"><span data-stu-id="af140-103">Gets ASR storage classification mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af140-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="af140-104">SYNTAX</span></span>

### <span data-ttu-id="af140-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="af140-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af140-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="af140-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af140-107">Opis</span><span class="sxs-lookup"><span data-stu-id="af140-107">DESCRIPTION</span></span>
<span data-ttu-id="af140-108">Polecenie cmdlet **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** pobiera szczegóły mapowania klasyfikacji magazynu ASR.</span><span class="sxs-lookup"><span data-stu-id="af140-108">The **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="af140-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="af140-109">EXAMPLES</span></span>

### <span data-ttu-id="af140-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="af140-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="af140-111">Wyświetl wszystkie mapowania klasyfikacji magazynu odpowiadające określonej klasyfikacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="af140-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="af140-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="af140-112">PARAMETERS</span></span>

### <span data-ttu-id="af140-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af140-113">-DefaultProfile</span></span>
<span data-ttu-id="af140-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="af140-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="af140-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="af140-115">-Name</span></span>
<span data-ttu-id="af140-116">Określa nazwę mapowania klasyfikacji magazynu, które ma zostać odzyskane.</span><span class="sxs-lookup"><span data-stu-id="af140-116">Specifies the name of the storage classification mapping to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af140-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="af140-117">-StorageClassification</span></span>
<span data-ttu-id="af140-118">Określa obiekt klasyfikacji magazynu ASR.</span><span class="sxs-lookup"><span data-stu-id="af140-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="af140-119">Polecenie cmdlet pobiera mapowania klasyfikacji magazynu ASR odpowiadające określonej klasyfikacji magazynu</span><span class="sxs-lookup"><span data-stu-id="af140-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af140-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af140-120">CommonParameters</span></span>
<span data-ttu-id="af140-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af140-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af140-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af140-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af140-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af140-123">INPUTS</span></span>

### <span data-ttu-id="af140-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="af140-124">None</span></span>

## <span data-ttu-id="af140-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="af140-125">OUTPUTS</span></span>

### <span data-ttu-id="af140-126">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="af140-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="af140-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="af140-127">NOTES</span></span>

## <span data-ttu-id="af140-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af140-128">RELATED LINKS</span></span>

[<span data-ttu-id="af140-129">Nowe — AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="af140-129">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="af140-130">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="af140-130">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
