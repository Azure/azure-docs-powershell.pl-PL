---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: 68c2914c694dbfb89044597fc35582a83f426b6c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341581"
---
# <span data-ttu-id="e6bc2-101">Copy-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e6bc2-101">Copy-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="e6bc2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e6bc2-102">SYNOPSIS</span></span>
<span data-ttu-id="e6bc2-103">Kopiuje dane z magazynu w jednym regionie do magazynu w innym regionie.</span><span class="sxs-lookup"><span data-stu-id="e6bc2-103">Copies data from a vault in one region to a vault in another region.</span></span>

## <span data-ttu-id="e6bc2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e6bc2-104">SYNTAX</span></span>

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## <span data-ttu-id="e6bc2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e6bc2-105">DESCRIPTION</span></span>
<span data-ttu-id="e6bc2-106">Polecenie cmdlet **copy-AzRecoveryServicesVault** kopiuje dane z magazynu w jednym regionie do magazynu w innym regionie.</span><span class="sxs-lookup"><span data-stu-id="e6bc2-106">The **Copy-AzRecoveryServicesVault** cmdlet copies data from a vault in one region to a vault in another region.</span></span> <span data-ttu-id="e6bc2-107">Obecnie obsługujemy tylko przenoszenie danych na poziomie magazynu.</span><span class="sxs-lookup"><span data-stu-id="e6bc2-107">Currently we only support vault level data move.</span></span>

## <span data-ttu-id="e6bc2-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e6bc2-108">EXAMPLES</span></span>

### <span data-ttu-id="e6bc2-109">Przykład 1: kopiowanie danych z vault1 do vault2</span><span class="sxs-lookup"><span data-stu-id="e6bc2-109">Example 1: Copy data from vault1 to vault2</span></span>
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```

<span data-ttu-id="e6bc2-110">Pierwszy z dwóch pierwszych apletów polecenia Pobierz magazyn usług Recovery Services-vault1 i vault2.</span><span class="sxs-lookup"><span data-stu-id="e6bc2-110">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="e6bc2-111">Drugie polecenie wyzwala pełne dane z vault1 do vault2.</span><span class="sxs-lookup"><span data-stu-id="e6bc2-111">The second command triggers a complete data move from vault1 to vault2.</span></span> 

### <span data-ttu-id="e6bc2-112">Przykład 2: kopiowanie danych z vault1 do vault2 tylko za pomocą elementów nieuszkodzonych</span><span class="sxs-lookup"><span data-stu-id="e6bc2-112">Example 2: Copy data from vault1 to vault2 with only failed items</span></span>
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
``` 

<span data-ttu-id="e6bc2-113">Pierwszy z dwóch pierwszych apletów polecenia Pobierz magazyn usług Recovery Services-vault1 i vault2.</span><span class="sxs-lookup"><span data-stu-id="e6bc2-113">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="e6bc2-114">Drugie polecenie wyzwala częściowe dane przenoszone z vault1 do vault2 z tylko elementami, które nie powiodły się w poprzednich operacjach przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="e6bc2-114">The second command triggers a partial data move from vault1 to vault2 with only those items which failed in previous move operations.</span></span>

## <span data-ttu-id="e6bc2-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e6bc2-115">PARAMETERS</span></span>

### <span data-ttu-id="e6bc2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6bc2-116">-DefaultProfile</span></span>
<span data-ttu-id="e6bc2-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e6bc2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6bc2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e6bc2-118">-Force</span></span>
<span data-ttu-id="e6bc2-119">Wymusza operację przenoszenia danych (zapobiega wyświetleniu okna dialogowego potwierdzenia) bez monitowania o potwierdzenie typu nadmiarowości miejsca do magazynowania w magazynie docelowym.</span><span class="sxs-lookup"><span data-stu-id="e6bc2-119">Forces the data move operation (prevents confirmation dialog) without asking confirmation for target vault storage redundancy type.</span></span> <span data-ttu-id="e6bc2-120">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e6bc2-120">This parameter is optional.</span></span> 

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

### <span data-ttu-id="e6bc2-121">-RetryOnlyFailed</span><span class="sxs-lookup"><span data-stu-id="e6bc2-121">-RetryOnlyFailed</span></span>
<span data-ttu-id="e6bc2-122">Parametr Przełącz umożliwiający przenoszenie danych tylko w przypadku kontenerów w magazynie źródłowym, które nie zostały jeszcze przeniesione.</span><span class="sxs-lookup"><span data-stu-id="e6bc2-122">Switch parameter to try data move only for containers in the source vault which are not yet moved.</span></span>

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

### <span data-ttu-id="e6bc2-123">-SourceVault</span><span class="sxs-lookup"><span data-stu-id="e6bc2-123">-SourceVault</span></span>
<span data-ttu-id="e6bc2-124">Obiekt magazynu źródłowego, który ma zostać przeniesiony.</span><span class="sxs-lookup"><span data-stu-id="e6bc2-124">The source vault object to be moved.</span></span>

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

### <span data-ttu-id="e6bc2-125">-TargetVault</span><span class="sxs-lookup"><span data-stu-id="e6bc2-125">-TargetVault</span></span>
<span data-ttu-id="e6bc2-126">Docelowy obiekt magazynu, w którym mają zostać przeniesione dane.</span><span class="sxs-lookup"><span data-stu-id="e6bc2-126">The target vault object where the data has to be moved.</span></span>

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

### <span data-ttu-id="e6bc2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6bc2-127">CommonParameters</span></span>
<span data-ttu-id="e6bc2-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6bc2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6bc2-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6bc2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6bc2-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6bc2-130">INPUTS</span></span>

### <span data-ttu-id="e6bc2-131">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="e6bc2-131">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="e6bc2-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e6bc2-132">OUTPUTS</span></span>

### <span data-ttu-id="e6bc2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e6bc2-133">System.String</span></span>

## <span data-ttu-id="e6bc2-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e6bc2-134">NOTES</span></span>

## <span data-ttu-id="e6bc2-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6bc2-135">RELATED LINKS</span></span>
