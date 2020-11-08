---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: e38a7b30622b8bb5dcbcf6912db7212465026687
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220440"
---
# <span data-ttu-id="fd7af-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="fd7af-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="fd7af-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fd7af-102">SYNOPSIS</span></span>
<span data-ttu-id="fd7af-103">Pobiera mapowania klasyfikacji magazynu ASR.</span><span class="sxs-lookup"><span data-stu-id="fd7af-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="fd7af-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fd7af-104">SYNTAX</span></span>

### <span data-ttu-id="fd7af-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fd7af-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd7af-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="fd7af-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd7af-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fd7af-107">DESCRIPTION</span></span>
<span data-ttu-id="fd7af-108">Polecenie cmdlet **Get-AzRecoveryServicesAsrStorageClassificationMapping** pobiera szczegóły mapowania klasyfikacji magazynu ASR.</span><span class="sxs-lookup"><span data-stu-id="fd7af-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="fd7af-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fd7af-109">EXAMPLES</span></span>

### <span data-ttu-id="fd7af-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fd7af-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="fd7af-111">Wyświetl wszystkie mapowania klasyfikacji magazynu odpowiadające określonej klasyfikacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="fd7af-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="fd7af-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fd7af-112">PARAMETERS</span></span>

### <span data-ttu-id="fd7af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd7af-113">-DefaultProfile</span></span>
<span data-ttu-id="fd7af-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd7af-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="fd7af-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fd7af-115">-Name</span></span>
<span data-ttu-id="fd7af-116">Określa nazwę mapowania klasyfikacji magazynu, które ma zostać odzyskane.</span><span class="sxs-lookup"><span data-stu-id="fd7af-116">Specifies the name of the storage classification mapping to get.</span></span>

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

### <span data-ttu-id="fd7af-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="fd7af-117">-StorageClassification</span></span>
<span data-ttu-id="fd7af-118">Określa obiekt klasyfikacji magazynu ASR.</span><span class="sxs-lookup"><span data-stu-id="fd7af-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="fd7af-119">Polecenie cmdlet pobiera mapowania klasyfikacji magazynu ASR odpowiadające określonej klasyfikacji magazynu</span><span class="sxs-lookup"><span data-stu-id="fd7af-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="fd7af-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd7af-120">CommonParameters</span></span>
<span data-ttu-id="fd7af-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd7af-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd7af-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd7af-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd7af-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd7af-123">INPUTS</span></span>

### <span data-ttu-id="fd7af-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="fd7af-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="fd7af-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fd7af-125">OUTPUTS</span></span>

### <span data-ttu-id="fd7af-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="fd7af-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="fd7af-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fd7af-127">NOTES</span></span>

## <span data-ttu-id="fd7af-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd7af-128">RELATED LINKS</span></span>

[<span data-ttu-id="fd7af-129">Nowe — AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="fd7af-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="fd7af-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="fd7af-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
