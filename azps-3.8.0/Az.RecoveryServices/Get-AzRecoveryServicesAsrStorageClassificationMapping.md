---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: e38a7b30622b8bb5dcbcf6912db7212465026687
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049571"
---
# <span data-ttu-id="0f2b6-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="0f2b6-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="0f2b6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0f2b6-102">SYNOPSIS</span></span>
<span data-ttu-id="0f2b6-103">Pobiera mapowania klasyfikacji magazynu ASR.</span><span class="sxs-lookup"><span data-stu-id="0f2b6-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="0f2b6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0f2b6-104">SYNTAX</span></span>

### <span data-ttu-id="0f2b6-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0f2b6-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f2b6-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="0f2b6-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0f2b6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0f2b6-107">DESCRIPTION</span></span>
<span data-ttu-id="0f2b6-108">Polecenie cmdlet **Get-AzRecoveryServicesAsrStorageClassificationMapping** pobiera szczegóły mapowania klasyfikacji magazynu ASR.</span><span class="sxs-lookup"><span data-stu-id="0f2b6-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="0f2b6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0f2b6-109">EXAMPLES</span></span>

### <span data-ttu-id="0f2b6-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0f2b6-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="0f2b6-111">Wyświetl wszystkie mapowania klasyfikacji magazynu odpowiadające określonej klasyfikacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="0f2b6-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="0f2b6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0f2b6-112">PARAMETERS</span></span>

### <span data-ttu-id="0f2b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f2b6-113">-DefaultProfile</span></span>
<span data-ttu-id="0f2b6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0f2b6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0f2b6-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0f2b6-115">-Name</span></span>
<span data-ttu-id="0f2b6-116">Określa nazwę mapowania klasyfikacji magazynu, które ma zostać odzyskane.</span><span class="sxs-lookup"><span data-stu-id="0f2b6-116">Specifies the name of the storage classification mapping to get.</span></span>

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

### <span data-ttu-id="0f2b6-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="0f2b6-117">-StorageClassification</span></span>
<span data-ttu-id="0f2b6-118">Określa obiekt klasyfikacji magazynu ASR.</span><span class="sxs-lookup"><span data-stu-id="0f2b6-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="0f2b6-119">Polecenie cmdlet pobiera mapowania klasyfikacji magazynu ASR odpowiadające określonej klasyfikacji magazynu</span><span class="sxs-lookup"><span data-stu-id="0f2b6-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="0f2b6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f2b6-120">CommonParameters</span></span>
<span data-ttu-id="0f2b6-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f2b6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f2b6-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f2b6-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f2b6-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f2b6-123">INPUTS</span></span>

### <span data-ttu-id="0f2b6-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="0f2b6-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="0f2b6-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0f2b6-125">OUTPUTS</span></span>

### <span data-ttu-id="0f2b6-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="0f2b6-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="0f2b6-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0f2b6-127">NOTES</span></span>

## <span data-ttu-id="0f2b6-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f2b6-128">RELATED LINKS</span></span>

[<span data-ttu-id="0f2b6-129">Nowe — AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="0f2b6-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="0f2b6-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="0f2b6-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
