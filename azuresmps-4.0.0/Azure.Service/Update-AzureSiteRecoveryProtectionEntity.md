---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 16146A0D-4605-489A-8259-A37BEAC98306
online version: ''
schema: 2.0.0
ms.openlocfilehash: 664c9af9373120f293153a1bbdc65d1a82637631
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054981"
---
# <span data-ttu-id="e7e3e-101">Update-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="e7e3e-101">Update-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="e7e3e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e7e3e-102">SYNOPSIS</span></span>
<span data-ttu-id="e7e3e-103">Aktualizuje właściwości jednostki ochrony w usłudze Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e7e3e-103">Updates the properties of a protection entity in Azure Site Recovery.</span></span>

## <span data-ttu-id="e7e3e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e7e3e-104">SYNTAX</span></span>

```
Update-AzureSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e7e3e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e7e3e-105">DESCRIPTION</span></span>
<span data-ttu-id="e7e3e-106">Polecenie cmdlet **Update-AzureSiteRecoveryProtectionEntity** aktualizuje właściwości jednostki ochrony w usłudze Azure Site Recovery, takie jak informacje o właścicielu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e7e3e-106">The **Update-AzureSiteRecoveryProtectionEntity** cmdlet updates the properties of a protection entity in Azure Site Recovery, such as virtual machine owner information.</span></span>
<span data-ttu-id="e7e3e-107">To polecenie cmdlet jest obsługiwane tylko w przypadku monitora maszyny wirtualnej (VMM) do chronionych obiektów ochrony przed programem VMM.</span><span class="sxs-lookup"><span data-stu-id="e7e3e-107">This cmdlet is supported only for Virtual Machine Monitor (VMM) to VMM protected protection entities.</span></span>

## <span data-ttu-id="e7e3e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e7e3e-108">EXAMPLES</span></span>

### <span data-ttu-id="e7e3e-109">Przykład 1: aktualizowanie jednostki ochrony</span><span class="sxs-lookup"><span data-stu-id="e7e3e-109">Example 1: Update a protection entity</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container
PS C:\> Update-AzureSiteRecoveryProtectionEntity -ProtectionEntity $ProtectionEntity
           Name             : 
           ID               : 680ffe0f-6236-465e-8c94-81242fa67e6d
           ClientRequestId  : 2c47e6ce-1460-4187-8a0f-b9073735fa38-2014-12-30 06:44:40Z-P
           State            : NotStarted
           StateDescription : NotStarted
           StartTime        : 
           EndTime          : 
           AllowedActions   : {}
           Tasks            : {}
           Errors           : {}
```

<span data-ttu-id="e7e3e-110">Pierwsze polecenie uzyskuje chroniony kontener za pomocą polecenia cmdlet **Get-AzureSiteRecoveryProtectionContainer** , a następnie zapisuje ten obiekt w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="e7e3e-110">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that object in the $Container variable.</span></span>

<span data-ttu-id="e7e3e-111">Drugie polecenie pobiera chronioną maszynę wirtualną należącej do kontenera przechowywanego w $Container przy użyciu polecenia cmdlet **Get-AzureSiteRecoveryProtectionEntity** , a następnie zapisuje ją w zmiennej $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="e7e3e-111">The second command gets the protected virtual machine that belongs to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet, and then stores it in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="e7e3e-112">Polecenie ostatnie umożliwia zaktualizowanie jednostki ochrony w $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="e7e3e-112">The final command updates the protection entity in $ProtectionEntity.</span></span>

## <span data-ttu-id="e7e3e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e7e3e-113">PARAMETERS</span></span>

### <span data-ttu-id="e7e3e-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="e7e3e-114">-Profile</span></span>
<span data-ttu-id="e7e3e-115">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7e3e-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e7e3e-116">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="e7e3e-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7e3e-117">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="e7e3e-117">-ProtectionEntity</span></span>
<span data-ttu-id="e7e3e-118">Określa jednostkę ochrony do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="e7e3e-118">Specifies a protection entity to update.</span></span>
<span data-ttu-id="e7e3e-119">Aby uzyskać obiekt **ASRProtectionEntity** , użyj polecenia cmdlet **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="e7e3e-119">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7e3e-120">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="e7e3e-120">-WaitForCompletion</span></span>
<span data-ttu-id="e7e3e-121">Wskazuje, że przed zwróceniem kontroli na konsolę programu Windows PowerShell to polecenie cmdlet oczekuje na ukończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="e7e3e-121">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="e7e3e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7e3e-122">CommonParameters</span></span>
<span data-ttu-id="e7e3e-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7e3e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7e3e-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7e3e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7e3e-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7e3e-125">INPUTS</span></span>

## <span data-ttu-id="e7e3e-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e7e3e-126">OUTPUTS</span></span>

## <span data-ttu-id="e7e3e-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e7e3e-127">NOTES</span></span>

## <span data-ttu-id="e7e3e-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7e3e-128">RELATED LINKS</span></span>

[<span data-ttu-id="e7e3e-129">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e7e3e-129">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="e7e3e-130">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="e7e3e-130">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="e7e3e-131">Set-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="e7e3e-131">Set-AzureSiteRecoveryProtectionEntity</span></span>](./Set-AzureSiteRecoveryProtectionEntity.md)


