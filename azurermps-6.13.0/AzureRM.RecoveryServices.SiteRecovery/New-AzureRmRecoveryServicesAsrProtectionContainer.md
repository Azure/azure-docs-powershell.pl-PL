---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: b551e89a800c70f1321a1f58cf4d5eae39fe69e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524317"
---
# <span data-ttu-id="20982-101">New-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="20982-101">New-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="20982-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="20982-102">SYNOPSIS</span></span>
<span data-ttu-id="20982-103">Tworzy kontener ochrony odzyskiwania witryny platformy Azure w określonej sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="20982-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20982-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="20982-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20982-105">Opis</span><span class="sxs-lookup"><span data-stu-id="20982-105">DESCRIPTION</span></span>
<span data-ttu-id="20982-106">Polecenie cmdlet New-AzureRmRecoveryServicesAsrProtectionContainer tworzy kontener ochrony pod określoną siecią szkieletową odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="20982-106">The New-AzureRmRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="20982-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="20982-107">EXAMPLES</span></span>

### <span data-ttu-id="20982-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="20982-108">Example 1</span></span>
```
PS C:\> $job = New-AzureRmRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="20982-109">Rozpoczyna Tworzenie kontenera ochrony z określonymi parametrami i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="20982-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="20982-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="20982-110">PARAMETERS</span></span>

### <span data-ttu-id="20982-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20982-111">-DefaultProfile</span></span>
<span data-ttu-id="20982-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="20982-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20982-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="20982-113">-InputObject</span></span>
<span data-ttu-id="20982-114">Tworzy kontener ochrony replikacji w podanym obiekcie wejściowym (Azure Fabric).</span><span class="sxs-lookup"><span data-stu-id="20982-114">Creates the replication protection container in specifed input Object (Azure Fabric).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20982-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="20982-115">-Name</span></span>
<span data-ttu-id="20982-116">Nazwa kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="20982-116">Name of the protection container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20982-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="20982-117">-Confirm</span></span>
<span data-ttu-id="20982-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20982-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20982-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20982-119">-WhatIf</span></span>
<span data-ttu-id="20982-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20982-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20982-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="20982-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20982-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20982-122">CommonParameters</span></span>
<span data-ttu-id="20982-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20982-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20982-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20982-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20982-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20982-125">INPUTS</span></span>

### <span data-ttu-id="20982-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="20982-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="20982-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="20982-127">OUTPUTS</span></span>

### <span data-ttu-id="20982-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="20982-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="20982-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="20982-129">NOTES</span></span>

## <span data-ttu-id="20982-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20982-130">RELATED LINKS</span></span>
