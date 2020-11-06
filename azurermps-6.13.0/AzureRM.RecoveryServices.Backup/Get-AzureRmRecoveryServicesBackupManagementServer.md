---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: c3419f020aca0853d94d8848e944e39fc8ed05a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544927"
---
# <span data-ttu-id="58ab4-101">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="58ab4-101">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="58ab4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58ab4-102">SYNOPSIS</span></span>
<span data-ttu-id="58ab4-103">Pobiera serwery usługi zarządzania zapasami SCDPM i Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="58ab4-103">Gets SCDPM and Azure Backup management servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58ab4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58ab4-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58ab4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="58ab4-105">DESCRIPTION</span></span>
<span data-ttu-id="58ab4-106">Polecenie cmdlet **Get-AzureRmRecoveryServicesBackupManagementServer** pobiera listę serwerów zarządzania zapasami, które są zarejestrowane w magazynie.</span><span class="sxs-lookup"><span data-stu-id="58ab4-106">The **Get-AzureRmRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>
<span data-ttu-id="58ab4-107">Istnieją dwa typy serwerów zarządzania kopiami zapasowymi: serwer System Center Data Protection Manager (SCDPM) i serwery zarządzania kopiami zapasowymi Azure.</span><span class="sxs-lookup"><span data-stu-id="58ab4-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="58ab4-108">Serwery zarządzania kopiami zapasowymi są instalowane osobno w celu zarządzania aranżacją kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="58ab4-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>
<span data-ttu-id="58ab4-109">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="58ab4-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="58ab4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58ab4-110">EXAMPLES</span></span>

### <span data-ttu-id="58ab4-111">Przykład 1: uzyskiwanie wszystkich serwerów zarządzania kopiami zapasowymi</span><span class="sxs-lookup"><span data-stu-id="58ab4-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupManagementServer
```

<span data-ttu-id="58ab4-112">To polecenie pobiera wszystkie serwery zarządzania zapasami zarejestrowane w magazynie.</span><span class="sxs-lookup"><span data-stu-id="58ab4-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="58ab4-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58ab4-113">PARAMETERS</span></span>

### <span data-ttu-id="58ab4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58ab4-114">-DefaultProfile</span></span>
<span data-ttu-id="58ab4-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="58ab4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58ab4-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="58ab4-116">-Name</span></span>
<span data-ttu-id="58ab4-117">Określa nazwę serwera zarządzania zapasami, którą należy uzyskać.</span><span class="sxs-lookup"><span data-stu-id="58ab4-117">Specifies the name of the Backup management server to get.</span></span>

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

### <span data-ttu-id="58ab4-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="58ab4-118">-VaultId</span></span>
<span data-ttu-id="58ab4-119">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="58ab4-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="58ab4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58ab4-120">CommonParameters</span></span>
<span data-ttu-id="58ab4-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58ab4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58ab4-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58ab4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58ab4-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58ab4-123">INPUTS</span></span>

### <span data-ttu-id="58ab4-124">System. String</span><span class="sxs-lookup"><span data-stu-id="58ab4-124">System.String</span></span>
<span data-ttu-id="58ab4-125">Parametry: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="58ab4-125">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="58ab4-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58ab4-126">OUTPUTS</span></span>

### <span data-ttu-id="58ab4-127">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="58ab4-127">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="58ab4-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58ab4-128">NOTES</span></span>

## <span data-ttu-id="58ab4-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58ab4-129">RELATED LINKS</span></span>

[<span data-ttu-id="58ab4-130">Wyrejestrowanie — AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="58ab4-130">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzureRmRecoveryServicesBackupManagementServer.md)


