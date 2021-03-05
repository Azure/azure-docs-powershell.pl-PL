---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: 5b4c7153a844bdc10d2ec487e51ef9f07be0c5c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960257"
---
# <span data-ttu-id="262ff-101">Copy-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="262ff-101">Copy-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="262ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="262ff-102">SYNOPSIS</span></span>
<span data-ttu-id="262ff-103">Kopiuje dane z magazynu w jednym regionie do magazynu w innym regionie.</span><span class="sxs-lookup"><span data-stu-id="262ff-103">Copies data from a vault in one region to a vault in another region.</span></span>

## <span data-ttu-id="262ff-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="262ff-104">SYNTAX</span></span>

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## <span data-ttu-id="262ff-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="262ff-105">DESCRIPTION</span></span>
<span data-ttu-id="262ff-106">Polecenie **cmdlet Copy-AzRecoveryServicesVault** kopiuje dane z magazynu w jednym regionie do magazynu w innym regionie.</span><span class="sxs-lookup"><span data-stu-id="262ff-106">The **Copy-AzRecoveryServicesVault** cmdlet copies data from a vault in one region to a vault in another region.</span></span> <span data-ttu-id="262ff-107">Obecnie obsługujemy tylko przenoszenie danych na poziomie magazynu.</span><span class="sxs-lookup"><span data-stu-id="262ff-107">Currently we only support vault level data move.</span></span>

## <span data-ttu-id="262ff-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="262ff-108">EXAMPLES</span></span>

### <span data-ttu-id="262ff-109">Przykład 1. Kopiowanie danych z magazynu 1 do magazynu2</span><span class="sxs-lookup"><span data-stu-id="262ff-109">Example 1: Copy data from vault1 to vault2</span></span>
```
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```

<span data-ttu-id="262ff-110">Pierwsze dwa polecenia cmdlet pobierają magazyn usług odzyskiwania — odpowiednio magazyn1 i magazyn2.</span><span class="sxs-lookup"><span data-stu-id="262ff-110">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="262ff-111">Drugie polecenie wyzwala pełne przeniesienie danych z magazynu 1 do magazynu2.</span><span class="sxs-lookup"><span data-stu-id="262ff-111">The second command triggers a complete data move from vault1 to vault2.</span></span> 

### <span data-ttu-id="262ff-112">Przykład 2. Kopiowanie danych z magazynu 1 do magazynu2 tylko z elementami, których niepowodzenie nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="262ff-112">Example 2: Copy data from vault1 to vault2 with only failed items</span></span>
```
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
```

<span data-ttu-id="262ff-113">Pierwsze dwa polecenia cmdlet pobierają magazyn usług odzyskiwania — odpowiednio magazyn1 i magazyn2.</span><span class="sxs-lookup"><span data-stu-id="262ff-113">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="262ff-114">Drugie polecenie wyzwala częściowe przeniesienie danych z magazynu 1 do magazynu2 tylko z tymi elementami, które nie powiodły się w poprzednich operacjach przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="262ff-114">The second command triggers a partial data move from vault1 to vault2 with only those items which failed in previous move operations.</span></span>

## <span data-ttu-id="262ff-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="262ff-115">PARAMETERS</span></span>

### <span data-ttu-id="262ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="262ff-116">-DefaultProfile</span></span>
<span data-ttu-id="262ff-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="262ff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262ff-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="262ff-118">-Force</span></span>
<span data-ttu-id="262ff-119">Wymusza operację przenoszenia danych (uniemożliwia okno dialogowe potwierdzenia) bez pytania o potwierdzenie dla docelowego typu nadmiarowości magazynu magazynu.</span><span class="sxs-lookup"><span data-stu-id="262ff-119">Forces the data move operation (prevents confirmation dialog) without asking confirmation for target vault storage redundancy type.</span></span> <span data-ttu-id="262ff-120">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="262ff-120">This parameter is optional.</span></span> 

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

### <span data-ttu-id="262ff-121">-RetryOnlyFailed</span><span class="sxs-lookup"><span data-stu-id="262ff-121">-RetryOnlyFailed</span></span>
<span data-ttu-id="262ff-122">Przełącz parametr, aby wypróbować przenoszenie danych tylko dla kontenerów w magazynie źródłowym, które nie zostały jeszcze przeniesione.</span><span class="sxs-lookup"><span data-stu-id="262ff-122">Switch parameter to try data move only for containers in the source vault which are not yet moved.</span></span>

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

### <span data-ttu-id="262ff-123">-SourceVault</span><span class="sxs-lookup"><span data-stu-id="262ff-123">-SourceVault</span></span>
<span data-ttu-id="262ff-124">Obiekt magazynu źródłowego, który ma zostać przeniesiony.</span><span class="sxs-lookup"><span data-stu-id="262ff-124">The source vault object to be moved.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="262ff-125">- TargetVault</span><span class="sxs-lookup"><span data-stu-id="262ff-125">-TargetVault</span></span>
<span data-ttu-id="262ff-126">Obiekt magazynu docelowego, do którego należy przenieść dane.</span><span class="sxs-lookup"><span data-stu-id="262ff-126">The target vault object where the data has to be moved.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="262ff-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="262ff-127">CommonParameters</span></span>
<span data-ttu-id="262ff-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="262ff-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="262ff-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="262ff-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="262ff-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="262ff-130">INPUTS</span></span>

### <span data-ttu-id="262ff-131">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="262ff-131">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="262ff-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="262ff-132">OUTPUTS</span></span>

### <span data-ttu-id="262ff-133">System.String</span><span class="sxs-lookup"><span data-stu-id="262ff-133">System.String</span></span>

## <span data-ttu-id="262ff-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="262ff-134">NOTES</span></span>

## <span data-ttu-id="262ff-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="262ff-135">RELATED LINKS</span></span>
