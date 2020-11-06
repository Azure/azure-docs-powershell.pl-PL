---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 1b025825878e2bc97837237e194b0ec37eb298d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550844"
---
# <span data-ttu-id="74e08-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="74e08-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="74e08-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="74e08-102">SYNOPSIS</span></span>
<span data-ttu-id="74e08-103">Wyrejestrowuje serwer SCDPM lub zapasowy serwer z magazynu.</span><span class="sxs-lookup"><span data-stu-id="74e08-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74e08-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="74e08-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74e08-105">Opis</span><span class="sxs-lookup"><span data-stu-id="74e08-105">DESCRIPTION</span></span>
<span data-ttu-id="74e08-106">Polecenie cmdlet **Unregister-AzureRmRecoveryServicesBackupManagementServer** Wyrejestrowuje serwer programu System Center Data Protection Manager (SCDPM) lub serwer kopii zapasowej Azure z magazynu.</span><span class="sxs-lookup"><span data-stu-id="74e08-106">The **Unregister-AzureRmRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="74e08-107">To polecenie cmdlet usuwa odwołania do serwerów, które nie są zarejestrowane w magazynie.</span><span class="sxs-lookup"><span data-stu-id="74e08-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>

<span data-ttu-id="74e08-108">Przed wyrejestrowaniem kontenera musisz usunąć wszelkie chronione dane skojarzone z tym kontenerem.</span><span class="sxs-lookup"><span data-stu-id="74e08-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

<span data-ttu-id="74e08-109">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="74e08-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="74e08-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="74e08-110">EXAMPLES</span></span>

### <span data-ttu-id="74e08-111">Przykład 1: Wyrejestrowanie serwera SCDPM z magazynu</span><span class="sxs-lookup"><span data-stu-id="74e08-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```
PS C:\>$BMS = Get-AzureRmRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupManagementServer -AzureRmBackupManagementServer $BMS
```

<span data-ttu-id="74e08-112">Pierwsze polecenie uzyskuje serwer zarządzania kopiami zapasowymi o nazwie dpmserver01.contoso.com, a następnie zapisuje go w zmiennej $BMS.</span><span class="sxs-lookup"><span data-stu-id="74e08-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>

<span data-ttu-id="74e08-113">Drugie polecenie Wyrejestrowuje serwer SCDPM z magazynu.</span><span class="sxs-lookup"><span data-stu-id="74e08-113">The second command unregisters the SCDPM server from the vault.</span></span>

## <span data-ttu-id="74e08-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="74e08-114">PARAMETERS</span></span>

### <span data-ttu-id="74e08-115">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="74e08-115">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="74e08-116">Określa obiekt serwera SCDPM do wyrejestrowania.</span><span class="sxs-lookup"><span data-stu-id="74e08-116">Specifies an SCDPM server object to unregister.</span></span>
<span data-ttu-id="74e08-117">Aby uzyskać obiekt **BackupManagementServer** , użyj polecenia cmdlet Get-AzureRmRecoveryServicesBackupManagementServer.</span><span class="sxs-lookup"><span data-stu-id="74e08-117">To obtain an **BackupManagementServer** object, use the Get-AzureRmRecoveryServicesBackupManagementServer cmdlet.</span></span>

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

### <span data-ttu-id="74e08-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74e08-118">-DefaultProfile</span></span>
<span data-ttu-id="74e08-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="74e08-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74e08-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74e08-120">CommonParameters</span></span>
<span data-ttu-id="74e08-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74e08-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74e08-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74e08-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74e08-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74e08-123">INPUTS</span></span>

## <span data-ttu-id="74e08-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="74e08-124">OUTPUTS</span></span>

## <span data-ttu-id="74e08-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="74e08-125">NOTES</span></span>

## <span data-ttu-id="74e08-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74e08-126">RELATED LINKS</span></span>

[<span data-ttu-id="74e08-127">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="74e08-127">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)


