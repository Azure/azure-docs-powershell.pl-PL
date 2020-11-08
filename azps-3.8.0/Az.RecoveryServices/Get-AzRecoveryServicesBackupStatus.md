---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupStatus.md
ms.openlocfilehash: 1e10fe2aa534e236c99468ec672e6a0eeadae469
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053685"
---
# <span data-ttu-id="c1ac4-101">Get-AzRecoveryServicesBackupStatus</span><span class="sxs-lookup"><span data-stu-id="c1ac4-101">Get-AzRecoveryServicesBackupStatus</span></span>

## <span data-ttu-id="c1ac4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c1ac4-102">SYNOPSIS</span></span>
<span data-ttu-id="c1ac4-103">Sprawdza, czy jest wykonywana kopia zapasowa zasobu ARM.</span><span class="sxs-lookup"><span data-stu-id="c1ac4-103">Checks whether your ARM resource is backed up or not.</span></span>

## <span data-ttu-id="c1ac4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c1ac4-104">SYNTAX</span></span>

### <span data-ttu-id="c1ac4-105">Nazwa (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="c1ac4-105">Name (Default)</span></span>
```
Get-AzRecoveryServicesBackupStatus -Name <String> -ResourceGroupName <String> -Type <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1ac4-106">IdWorkload</span><span class="sxs-lookup"><span data-stu-id="c1ac4-106">IdWorkload</span></span>
```
Get-AzRecoveryServicesBackupStatus -Type <String> -ResourceId <String> -ProtectableObjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1ac4-107">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="c1ac4-107">Id</span></span>
```
Get-AzRecoveryServicesBackupStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1ac4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c1ac4-108">DESCRIPTION</span></span>
<span data-ttu-id="c1ac4-109">Polecenie zwraca wartość null/jest puste, jeśli określony zasób nie jest chroniony w ramach żadnego magazynu usług Recovery Services w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c1ac4-109">The command returns null/empty if the specified resource is not protected under any Recovery Services vault in the subscription.</span></span> <span data-ttu-id="c1ac4-110">Jeśli jest chroniony, zostaną zwrócone odpowiednie szczegóły dotyczące magazynu.</span><span class="sxs-lookup"><span data-stu-id="c1ac4-110">If it is protected, the relevant vault details will be returned.</span></span>

## <span data-ttu-id="c1ac4-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c1ac4-111">EXAMPLES</span></span>

### <span data-ttu-id="c1ac4-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c1ac4-112">Example 1</span></span>
```
PS C:\> $status = Get-AzRecoveryServicesBackupStatus -Name "myAzureVM" -ResourceGroupName "myAzureVMRG" -ResourceType "AzureVM"
PS C:\> If ($status.BackedUp -eq $false) {
$vault = Get-AzRecoveryServicesVault -Name "testvault" -ResourceGroupName "vaultResourceGroup"
$defPolicy = Get-AzRecoveryServicesBackupProtectionPolicy -Vault $vault -WorkloadType "AzureVM"
Enable-AzRecoveryServicesBackupProtection -Vault $vault -Policy $defpol -Name "myAzureVM" -ResourceGroupName "myAzureVMRG"
}
```

## <span data-ttu-id="c1ac4-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c1ac4-113">PARAMETERS</span></span>

### <span data-ttu-id="c1ac4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1ac4-114">-DefaultProfile</span></span>
<span data-ttu-id="c1ac4-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c1ac4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1ac4-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c1ac4-116">-Name</span></span>
<span data-ttu-id="c1ac4-117">Nazwa zasobu platformy Azure, którego element reprezentatywny musi zostać sprawdzony, jeśli jest już chroniony przez jakiś magazyn usług Recovery Services w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c1ac4-117">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ac4-118">-ProtectableObjectName</span><span class="sxs-lookup"><span data-stu-id="c1ac4-118">-ProtectableObjectName</span></span>
<span data-ttu-id="c1ac4-119">Nazwa zasobu platformy Azure, którego element reprezentatywny musi zostać sprawdzony, jeśli jest już chroniony przez jakiś magazyn usług Recovery Services w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c1ac4-119">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: IdWorkload
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ac4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1ac4-120">-ResourceGroupName</span></span>
<span data-ttu-id="c1ac4-121">Nazwa grupy zasobów zasobu platformy Azure, której element reprezentatywny musi zostać sprawdzony, jeśli jest już chroniony przez jakiś magazyn RecoveryServices w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c1ac4-121">Name of the resource group of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ac4-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1ac4-122">-ResourceId</span></span>
<span data-ttu-id="c1ac4-123">Identyfikator zasobu platformy Azure, którego element reprezentatywny musi zostać sprawdzony, jeśli jest już chroniony przez jakiś magazyn RecoveryServices w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c1ac4-123">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: IdWorkload, Id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ac4-124">-Type</span><span class="sxs-lookup"><span data-stu-id="c1ac4-124">-Type</span></span>
<span data-ttu-id="c1ac4-125">Nazwa zasobu platformy Azure, którego element reprezentatywny musi zostać sprawdzony, jeśli jest już chroniony przez jakiś magazyn usług Recovery Services w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c1ac4-125">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, IdWorkload
Aliases:
Accepted values: AzureVM, AzureFiles

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ac4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1ac4-126">CommonParameters</span></span>
<span data-ttu-id="c1ac4-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1ac4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1ac4-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1ac4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1ac4-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1ac4-129">INPUTS</span></span>

### <span data-ttu-id="c1ac4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c1ac4-130">System.String</span></span>

## <span data-ttu-id="c1ac4-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c1ac4-131">OUTPUTS</span></span>

### <span data-ttu-id="c1ac4-132">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ResourceBackupStatus</span><span class="sxs-lookup"><span data-stu-id="c1ac4-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ResourceBackupStatus</span></span>

## <span data-ttu-id="c1ac4-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c1ac4-133">NOTES</span></span>

## <span data-ttu-id="c1ac4-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c1ac4-134">RELATED LINKS</span></span>
