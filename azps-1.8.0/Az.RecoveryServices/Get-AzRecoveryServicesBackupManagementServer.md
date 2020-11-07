---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 341b222c8b5e85a4b5f5221c34d6f45cd2993c71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708669"
---
# <span data-ttu-id="945a7-101">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="945a7-101">Get-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="945a7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="945a7-102">SYNOPSIS</span></span>
<span data-ttu-id="945a7-103">Pobiera serwery usługi zarządzania zapasami SCDPM i Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="945a7-103">Gets SCDPM and Azure Backup management servers.</span></span>

## <span data-ttu-id="945a7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="945a7-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="945a7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="945a7-105">DESCRIPTION</span></span>
<span data-ttu-id="945a7-106">Polecenie cmdlet **Get-AzRecoveryServicesBackupManagementServer** pobiera listę serwerów zarządzania zapasami, które są zarejestrowane w magazynie.</span><span class="sxs-lookup"><span data-stu-id="945a7-106">The **Get-AzRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>
<span data-ttu-id="945a7-107">Istnieją dwa typy serwerów zarządzania kopiami zapasowymi: serwer System Center Data Protection Manager (SCDPM) i serwery zarządzania kopiami zapasowymi Azure.</span><span class="sxs-lookup"><span data-stu-id="945a7-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="945a7-108">Serwery zarządzania kopiami zapasowymi są instalowane osobno w celu zarządzania aranżacją kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="945a7-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>
<span data-ttu-id="945a7-109">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="945a7-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="945a7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="945a7-110">EXAMPLES</span></span>

### <span data-ttu-id="945a7-111">Przykład 1: uzyskiwanie wszystkich serwerów zarządzania kopiami zapasowymi</span><span class="sxs-lookup"><span data-stu-id="945a7-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupManagementServer
```

<span data-ttu-id="945a7-112">To polecenie pobiera wszystkie serwery zarządzania zapasami zarejestrowane w magazynie.</span><span class="sxs-lookup"><span data-stu-id="945a7-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="945a7-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="945a7-113">PARAMETERS</span></span>

### <span data-ttu-id="945a7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="945a7-114">-DefaultProfile</span></span>
<span data-ttu-id="945a7-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="945a7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="945a7-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="945a7-116">-Name</span></span>
<span data-ttu-id="945a7-117">Określa nazwę serwera zarządzania zapasami, którą należy uzyskać.</span><span class="sxs-lookup"><span data-stu-id="945a7-117">Specifies the name of the Backup management server to get.</span></span>

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

### <span data-ttu-id="945a7-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="945a7-118">-VaultId</span></span>
<span data-ttu-id="945a7-119">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="945a7-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="945a7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="945a7-120">CommonParameters</span></span>
<span data-ttu-id="945a7-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="945a7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="945a7-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="945a7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="945a7-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="945a7-123">INPUTS</span></span>

### <span data-ttu-id="945a7-124">System. String</span><span class="sxs-lookup"><span data-stu-id="945a7-124">System.String</span></span>

## <span data-ttu-id="945a7-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="945a7-125">OUTPUTS</span></span>

### <span data-ttu-id="945a7-126">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="945a7-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="945a7-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="945a7-127">NOTES</span></span>

## <span data-ttu-id="945a7-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="945a7-128">RELATED LINKS</span></span>

[<span data-ttu-id="945a7-129">Wyrejestrowanie — AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="945a7-129">Unregister-AzRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzRecoveryServicesBackupManagementServer.md)


