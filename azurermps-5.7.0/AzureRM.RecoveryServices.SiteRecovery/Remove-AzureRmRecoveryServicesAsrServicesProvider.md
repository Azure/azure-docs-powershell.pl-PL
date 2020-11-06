---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 2aa8855365ea74a00df875fb62bfec49a8c591ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544223"
---
# <span data-ttu-id="96971-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="96971-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="96971-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="96971-102">SYNOPSIS</span></span>
<span data-ttu-id="96971-103">Usuwa/wyrejestrowuje określonego dostawcę usług odzyskiwania usługi Azure Site Recovery z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="96971-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96971-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="96971-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96971-105">Opis</span><span class="sxs-lookup"><span data-stu-id="96971-105">DESCRIPTION</span></span>
<span data-ttu-id="96971-106">Polecenie cmdlet **Remove-AzureRmRecoveryServicesAsrServicesProvider** usuwa określonego dostawcę usług odzyskiwania usługi Azure Site Recovery z magazynu.</span><span class="sxs-lookup"><span data-stu-id="96971-106">The **Remove-AzureRmRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="96971-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="96971-107">EXAMPLES</span></span>

### <span data-ttu-id="96971-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="96971-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="96971-109">Rozpoczyna usuwanie/Wyrejestrowanie określonego dostawcy usług Azure Site Recovery Services i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="96971-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="96971-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="96971-110">PARAMETERS</span></span>

### <span data-ttu-id="96971-111">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="96971-111">-Confirm</span></span>
<span data-ttu-id="96971-112">Określ, czy potwierdzenie jest wymagane.</span><span class="sxs-lookup"><span data-stu-id="96971-112">Specify if confirmation is required.</span></span> <span data-ttu-id="96971-113">Ustaw wartość parametru Confirm na $false, aby pominąć potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="96971-113">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96971-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96971-114">-DefaultProfile</span></span>
<span data-ttu-id="96971-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="96971-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="96971-116">-Force</span><span class="sxs-lookup"><span data-stu-id="96971-116">-Force</span></span>
<span data-ttu-id="96971-117">Wymuś uruchomienie polecenia bez podania dodatkowego ostrzeżenia.</span><span class="sxs-lookup"><span data-stu-id="96971-117">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96971-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="96971-118">-InputObject</span></span>
<span data-ttu-id="96971-119">Obiekt wejściowy do polecenia cmdlet: obiekt dostawcy usług odzyskiwania ASR odpowiadający dostawcy usług odzyskiwania ASR, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="96971-119">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96971-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96971-120">-WhatIf</span></span>
<span data-ttu-id="96971-121">Pokazuje, co się stanie, jeśli jest wykonywane polecenie cmdlet bez faktycznego wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96971-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96971-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96971-122">CommonParameters</span></span>
<span data-ttu-id="96971-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96971-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96971-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96971-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96971-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96971-125">INPUTS</span></span>

### <span data-ttu-id="96971-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="96971-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="96971-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="96971-127">OUTPUTS</span></span>

### <span data-ttu-id="96971-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="96971-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="96971-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="96971-129">NOTES</span></span>

## <span data-ttu-id="96971-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="96971-130">RELATED LINKS</span></span>

[<span data-ttu-id="96971-131">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="96971-131">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="96971-132">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="96971-132">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
