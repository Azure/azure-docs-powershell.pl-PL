---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/unregister-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 5452758a5cf269ef50475b8962e5fbca117dbb1d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93886569"
---
# <span data-ttu-id="31e7c-101">Unregister-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="31e7c-101">Unregister-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="31e7c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="31e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="31e7c-103">Wyrejestrowuje serwer SCDPM lub zapasowy serwer z magazynu.</span><span class="sxs-lookup"><span data-stu-id="31e7c-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

## <span data-ttu-id="31e7c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="31e7c-104">SYNTAX</span></span>

```
Unregister-AzRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="31e7c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="31e7c-105">DESCRIPTION</span></span>
<span data-ttu-id="31e7c-106">Polecenie cmdlet **Unregister-AzRecoveryServicesBackupManagementServer** Wyrejestrowuje serwer programu System Center Data Protection Manager (SCDPM) lub serwer kopii zapasowej Azure z magazynu.</span><span class="sxs-lookup"><span data-stu-id="31e7c-106">The **Unregister-AzRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="31e7c-107">To polecenie cmdlet usuwa odwołania do serwerów, które nie są zarejestrowane w magazynie.</span><span class="sxs-lookup"><span data-stu-id="31e7c-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>
<span data-ttu-id="31e7c-108">Przed wyrejestrowaniem kontenera musisz usunąć wszelkie chronione dane skojarzone z tym kontenerem.</span><span class="sxs-lookup"><span data-stu-id="31e7c-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="31e7c-109">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="31e7c-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="31e7c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="31e7c-110">EXAMPLES</span></span>

### <span data-ttu-id="31e7c-111">Przykład 1: Wyrejestrowanie serwera SCDPM z magazynu</span><span class="sxs-lookup"><span data-stu-id="31e7c-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```
PS C:\>$BMS = Get-AzRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzRecoveryServicesBackupManagementServer -AzBackupManagementServer $BMS
```

<span data-ttu-id="31e7c-112">Pierwsze polecenie uzyskuje serwer zarządzania kopiami zapasowymi o nazwie dpmserver01.contoso.com, a następnie zapisuje go w zmiennej $BMS.</span><span class="sxs-lookup"><span data-stu-id="31e7c-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>
<span data-ttu-id="31e7c-113">Drugie polecenie Wyrejestrowuje serwer SCDPM z magazynu.</span><span class="sxs-lookup"><span data-stu-id="31e7c-113">The second command unregisters the SCDPM server from the vault.</span></span>

## <span data-ttu-id="31e7c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="31e7c-114">PARAMETERS</span></span>

### <span data-ttu-id="31e7c-115">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="31e7c-115">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="31e7c-116">Kontener kopii zapasowych usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="31e7c-116">The recovery services backup container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e7c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31e7c-117">-DefaultProfile</span></span>
<span data-ttu-id="31e7c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="31e7c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31e7c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31e7c-119">-PassThru</span></span>
<span data-ttu-id="31e7c-120">Zwraca serwer zarządzania kopiami zapasowymi, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="31e7c-120">Return the Backup Management Server to be deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e7c-121">-VaultId</span><span class="sxs-lookup"><span data-stu-id="31e7c-121">-VaultId</span></span>
<span data-ttu-id="31e7c-122">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="31e7c-122">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="31e7c-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="31e7c-123">-Confirm</span></span>
<span data-ttu-id="31e7c-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31e7c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31e7c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31e7c-125">-WhatIf</span></span>
<span data-ttu-id="31e7c-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31e7c-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31e7c-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="31e7c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31e7c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31e7c-128">CommonParameters</span></span>
<span data-ttu-id="31e7c-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31e7c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31e7c-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31e7c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31e7c-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31e7c-131">INPUTS</span></span>

### <span data-ttu-id="31e7c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="31e7c-132">System.String</span></span>

## <span data-ttu-id="31e7c-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="31e7c-133">OUTPUTS</span></span>

### <span data-ttu-id="31e7c-134">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="31e7c-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="31e7c-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="31e7c-135">NOTES</span></span>

## <span data-ttu-id="31e7c-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31e7c-136">RELATED LINKS</span></span>

[<span data-ttu-id="31e7c-137">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="31e7c-137">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)


