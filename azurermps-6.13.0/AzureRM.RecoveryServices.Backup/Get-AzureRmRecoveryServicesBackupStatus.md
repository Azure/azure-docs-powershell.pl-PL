---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupStatus.md
ms.openlocfilehash: 00d7bb2c58abfa466b0c4843eb480b43b08b3d90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718285"
---
# <span data-ttu-id="82652-101">Get-AzureRmRecoveryServicesBackupStatus</span><span class="sxs-lookup"><span data-stu-id="82652-101">Get-AzureRmRecoveryServicesBackupStatus</span></span>

## <span data-ttu-id="82652-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="82652-102">SYNOPSIS</span></span>
<span data-ttu-id="82652-103">Sprawdza, czy jest wykonywana kopia zapasowa zasobu ARM.</span><span class="sxs-lookup"><span data-stu-id="82652-103">Checks whether your ARM resource is backed up or not.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82652-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="82652-104">SYNTAX</span></span>

### <span data-ttu-id="82652-105">Nazwa (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="82652-105">Name (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupStatus -Name <String> -ResourceGroupName <String> -Type <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82652-106">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="82652-106">Id</span></span>
```
Get-AzureRmRecoveryServicesBackupStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="82652-107">Opis</span><span class="sxs-lookup"><span data-stu-id="82652-107">DESCRIPTION</span></span>
<span data-ttu-id="82652-108">Polecenie zwraca wartość null/jest puste, jeśli określony zasób nie jest chroniony w ramach żadnego magazynu usług Recovery Services w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="82652-108">The command returns null/empty if the specified resource is not protected under any Recovery Services vault in the subscription.</span></span> <span data-ttu-id="82652-109">Jeśli jest chroniony, zostaną zwrócone odpowiednie szczegóły dotyczące magazynu.</span><span class="sxs-lookup"><span data-stu-id="82652-109">If it is protected, the relevant vault details will be returned.</span></span>

## <span data-ttu-id="82652-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="82652-110">EXAMPLES</span></span>

### <span data-ttu-id="82652-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="82652-111">Example 1</span></span>
```
PS C:\> $status = Get-AzureRmRecoveryServicesBackupStatus -Name "myAzureVM" -ResourceGroupName "myAzureVMRG" -ResourceType "AzureVM"
PS C:\> If ($status.BackedUp -eq $false) {
$vault = Get-AzureRmRecoveryServicesVault -Name "testvault" -ResourceGroupName "vaultResourceGroup"
$defPolicy = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Vault $vault -WorkloadType "AzureVM"
Enable-AzureRmRecoveryServicesBackupProtection -Vault $vault -Policy $defpol -Name "myAzureVM" -ResourceGroupName "myAzureVMRG"
}
```

## <span data-ttu-id="82652-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="82652-112">PARAMETERS</span></span>

### <span data-ttu-id="82652-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82652-113">-DefaultProfile</span></span>
<span data-ttu-id="82652-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="82652-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82652-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="82652-115">-Name</span></span>
<span data-ttu-id="82652-116">Nazwa zasobu platformy Azure, którego element reprezentatywny musi zostać sprawdzony, jeśli jest już chroniony przez jakiś magazyn usług Recovery Services w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="82652-116">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

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

### <span data-ttu-id="82652-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82652-117">-ResourceGroupName</span></span>
<span data-ttu-id="82652-118">Nazwa grupy zasobów zasobu platformy Azure, której element reprezentatywny musi zostać sprawdzony, jeśli jest już chroniony przez jakiś magazyn RecoveryServices w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="82652-118">Name of the resource group of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="82652-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82652-119">-ResourceId</span></span>
<span data-ttu-id="82652-120">Identyfikator zasobu platformy Azure, którego element reprezentatywny musi zostać sprawdzony, jeśli jest już chroniony przez jakiś magazyn RecoveryServices w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="82652-120">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82652-121">-Type</span><span class="sxs-lookup"><span data-stu-id="82652-121">-Type</span></span>
<span data-ttu-id="82652-122">Nazwa zasobu platformy Azure, którego element reprezentatywny musi zostać sprawdzony, jeśli jest już chroniony przez jakiś magazyn usług Recovery Services w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="82652-122">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:
Accepted values: AzureVM, AzureFiles

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82652-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82652-123">CommonParameters</span></span>
<span data-ttu-id="82652-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82652-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82652-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82652-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82652-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82652-126">INPUTS</span></span>

### <span data-ttu-id="82652-127">System. String</span><span class="sxs-lookup"><span data-stu-id="82652-127">System.String</span></span>

## <span data-ttu-id="82652-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="82652-128">OUTPUTS</span></span>

### <span data-ttu-id="82652-129">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ResourceBackupStatus</span><span class="sxs-lookup"><span data-stu-id="82652-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ResourceBackupStatus</span></span>

## <span data-ttu-id="82652-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="82652-130">NOTES</span></span>

## <span data-ttu-id="82652-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="82652-131">RELATED LINKS</span></span>
