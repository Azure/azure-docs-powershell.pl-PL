---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: 630dc1a3a14beec147dec3f7bd2601ed0666ad78
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232691"
---
# <span data-ttu-id="ded4c-101">Copy-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ded4c-101">Copy-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="ded4c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ded4c-102">SYNOPSIS</span></span>
<span data-ttu-id="ded4c-103">Kopiuje dane z magazynu w jednym regionie do magazynu w innym regionie.</span><span class="sxs-lookup"><span data-stu-id="ded4c-103">Copies data from a vault in one region to a vault in another region.</span></span>

## <span data-ttu-id="ded4c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ded4c-104">SYNTAX</span></span>

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## <span data-ttu-id="ded4c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ded4c-105">DESCRIPTION</span></span>
<span data-ttu-id="ded4c-106">Polecenie cmdlet **copy-AzRecoveryServicesVault** kopiuje dane z magazynu w jednym regionie do magazynu w innym regionie.</span><span class="sxs-lookup"><span data-stu-id="ded4c-106">The **Copy-AzRecoveryServicesVault** cmdlet copies data from a vault in one region to a vault in another region.</span></span> <span data-ttu-id="ded4c-107">Obecnie obsługujemy tylko przenoszenie danych na poziomie magazynu.</span><span class="sxs-lookup"><span data-stu-id="ded4c-107">Currently we only support vault level data move.</span></span>

## <span data-ttu-id="ded4c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ded4c-108">EXAMPLES</span></span>

### <span data-ttu-id="ded4c-109">Przykład 1: kopiowanie danych z vault1 do vault2</span><span class="sxs-lookup"><span data-stu-id="ded4c-109">Example 1: Copy data from vault1 to vault2</span></span>
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```git 

The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.
The second command triggers a complete data move from vault1 to vault2. 

### Example 2: Copy data from vault1 to vault2 with only failed items
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
```git 

The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.
The second command triggers a partial data move from vault1 to vault2 with only those items which failed in previous move operations.

## PARAMETERS

### -DefaultProfile
The credentials, account, tenant, and subscription used for communication with Azure.

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

### <span data-ttu-id="ded4c-110">-Force</span><span class="sxs-lookup"><span data-stu-id="ded4c-110">-Force</span></span>
<span data-ttu-id="ded4c-111">Wymusza operację przenoszenia danych (zapobiega wyświetleniu okna dialogowego potwierdzenia) bez monitowania o potwierdzenie typu nadmiarowości miejsca do magazynowania w magazynie docelowym.</span><span class="sxs-lookup"><span data-stu-id="ded4c-111">Forces the data move operation (prevents confirmation dialog) without asking confirmation for target vault storage redundancy type.</span></span> <span data-ttu-id="ded4c-112">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="ded4c-112">This parameter is optional.</span></span> 

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

### <span data-ttu-id="ded4c-113">-RetryOnlyFailed</span><span class="sxs-lookup"><span data-stu-id="ded4c-113">-RetryOnlyFailed</span></span>
<span data-ttu-id="ded4c-114">Parametr Przełącz umożliwiający przenoszenie danych tylko w przypadku kontenerów w magazynie źródłowym, które nie zostały jeszcze przeniesione.</span><span class="sxs-lookup"><span data-stu-id="ded4c-114">Switch parameter to try data move only for containers in the source vault which are not yet moved.</span></span>

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

### <span data-ttu-id="ded4c-115">-SourceVault</span><span class="sxs-lookup"><span data-stu-id="ded4c-115">-SourceVault</span></span>
<span data-ttu-id="ded4c-116">Obiekt magazynu źródłowego, który ma zostać przeniesiony.</span><span class="sxs-lookup"><span data-stu-id="ded4c-116">The source vault object to be moved.</span></span>

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

### <span data-ttu-id="ded4c-117">-TargetVault</span><span class="sxs-lookup"><span data-stu-id="ded4c-117">-TargetVault</span></span>
<span data-ttu-id="ded4c-118">Docelowy obiekt magazynu, w którym mają zostać przeniesione dane.</span><span class="sxs-lookup"><span data-stu-id="ded4c-118">The target vault object where the data has to be moved.</span></span>

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

### <span data-ttu-id="ded4c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ded4c-119">CommonParameters</span></span>
<span data-ttu-id="ded4c-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ded4c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ded4c-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ded4c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ded4c-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ded4c-122">INPUTS</span></span>

### <span data-ttu-id="ded4c-123">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="ded4c-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="ded4c-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ded4c-124">OUTPUTS</span></span>

### <span data-ttu-id="ded4c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ded4c-125">System.String</span></span>

## <span data-ttu-id="ded4c-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ded4c-126">NOTES</span></span>

## <span data-ttu-id="ded4c-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ded4c-127">RELATED LINKS</span></span>
