---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 50fb3af805adf4e42ab0b6bf1824b09473d98239
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990879"
---
# <span data-ttu-id="42c43-101">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="42c43-101">Get-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="42c43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42c43-102">SYNOPSIS</span></span>
<span data-ttu-id="42c43-103">Pobiera serwery zarządzania kopiami scdpm i kopiami zapasowymi platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="42c43-103">Gets SCDPM and Azure Backup management servers.</span></span>

## <span data-ttu-id="42c43-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="42c43-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42c43-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="42c43-105">DESCRIPTION</span></span>
<span data-ttu-id="42c43-106">Polecenie **cmdlet Get-AzRecoveryServicesBackupManagementServer** pobiera listę serwerów zarządzania kopiami zapasowymi zarejestrowanymi w magazynie.</span><span class="sxs-lookup"><span data-stu-id="42c43-106">The **Get-AzRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>
<span data-ttu-id="42c43-107">Istnieją dwa typy serwerów zarządzania kopiami zapasowymi: system Center Data Protection Manager (SCDPM) i serwery zarządzania kopiami zapasowymi azure.</span><span class="sxs-lookup"><span data-stu-id="42c43-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="42c43-108">Serwery zarządzania kopiami zapasowymi są instalowane oddzielnie, aby zarządzać kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="42c43-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>
<span data-ttu-id="42c43-109">Ustaw kontekst magazynu za pomocą Set-AzRecoveryServicesVaultContext cmdlet przed użyciem bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42c43-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="42c43-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="42c43-110">EXAMPLES</span></span>

### <span data-ttu-id="42c43-111">Przykład 1. Uzyskiwanie wszystkich serwerów zarządzania kopiami zapasowymi</span><span class="sxs-lookup"><span data-stu-id="42c43-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupManagementServer
```

<span data-ttu-id="42c43-112">To polecenie pobiera wszystkie serwery zarządzania kopiami zapasowymi zarejestrowane w magazynie.</span><span class="sxs-lookup"><span data-stu-id="42c43-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="42c43-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42c43-113">PARAMETERS</span></span>

### <span data-ttu-id="42c43-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42c43-114">-DefaultProfile</span></span>
<span data-ttu-id="42c43-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="42c43-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42c43-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="42c43-116">-Name</span></span>
<span data-ttu-id="42c43-117">Określa nazwę serwera zarządzania kopiami zapasowymi do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="42c43-117">Specifies the name of the Backup management server to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42c43-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="42c43-118">-VaultId</span></span>
<span data-ttu-id="42c43-119">ARM identyfikatora magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="42c43-119">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42c43-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42c43-120">CommonParameters</span></span>
<span data-ttu-id="42c43-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42c43-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42c43-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="42c43-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42c43-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42c43-123">INPUTS</span></span>

### <span data-ttu-id="42c43-124">System.String</span><span class="sxs-lookup"><span data-stu-id="42c43-124">System.String</span></span>

## <span data-ttu-id="42c43-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42c43-125">OUTPUTS</span></span>

### <span data-ttu-id="42c43-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="42c43-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="42c43-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="42c43-127">NOTES</span></span>

## <span data-ttu-id="42c43-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42c43-128">RELATED LINKS</span></span>

[<span data-ttu-id="42c43-129">Unregister-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="42c43-129">Unregister-AzRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzRecoveryServicesBackupManagementServer.md)


