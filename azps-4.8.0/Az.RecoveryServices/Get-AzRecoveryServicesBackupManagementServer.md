---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 09d27926f489feea397c98a217840bb973e002ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063846"
---
# <span data-ttu-id="d383b-101">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="d383b-101">Get-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="d383b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d383b-102">SYNOPSIS</span></span>
<span data-ttu-id="d383b-103">Pobiera serwery usługi zarządzania zapasami SCDPM i Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="d383b-103">Gets SCDPM and Azure Backup management servers.</span></span>

## <span data-ttu-id="d383b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d383b-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d383b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d383b-105">DESCRIPTION</span></span>
<span data-ttu-id="d383b-106">Polecenie cmdlet **Get-AzRecoveryServicesBackupManagementServer** pobiera listę serwerów zarządzania zapasami, które są zarejestrowane w magazynie.</span><span class="sxs-lookup"><span data-stu-id="d383b-106">The **Get-AzRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>
<span data-ttu-id="d383b-107">Istnieją dwa typy serwerów zarządzania kopiami zapasowymi: serwer System Center Data Protection Manager (SCDPM) i serwery zarządzania kopiami zapasowymi Azure.</span><span class="sxs-lookup"><span data-stu-id="d383b-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="d383b-108">Serwery zarządzania kopiami zapasowymi są instalowane osobno w celu zarządzania aranżacją kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="d383b-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>
<span data-ttu-id="d383b-109">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="d383b-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="d383b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d383b-110">EXAMPLES</span></span>

### <span data-ttu-id="d383b-111">Przykład 1: uzyskiwanie wszystkich serwerów zarządzania kopiami zapasowymi</span><span class="sxs-lookup"><span data-stu-id="d383b-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupManagementServer
```

<span data-ttu-id="d383b-112">To polecenie pobiera wszystkie serwery zarządzania zapasami zarejestrowane w magazynie.</span><span class="sxs-lookup"><span data-stu-id="d383b-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="d383b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d383b-113">PARAMETERS</span></span>

### <span data-ttu-id="d383b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d383b-114">-DefaultProfile</span></span>
<span data-ttu-id="d383b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d383b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d383b-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d383b-116">-Name</span></span>
<span data-ttu-id="d383b-117">Określa nazwę serwera zarządzania zapasami, którą należy uzyskać.</span><span class="sxs-lookup"><span data-stu-id="d383b-117">Specifies the name of the Backup management server to get.</span></span>

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

### <span data-ttu-id="d383b-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d383b-118">-VaultId</span></span>
<span data-ttu-id="d383b-119">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="d383b-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="d383b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d383b-120">CommonParameters</span></span>
<span data-ttu-id="d383b-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d383b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d383b-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d383b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d383b-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d383b-123">INPUTS</span></span>

### <span data-ttu-id="d383b-124">System. String</span><span class="sxs-lookup"><span data-stu-id="d383b-124">System.String</span></span>

## <span data-ttu-id="d383b-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d383b-125">OUTPUTS</span></span>

### <span data-ttu-id="d383b-126">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="d383b-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="d383b-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d383b-127">NOTES</span></span>

## <span data-ttu-id="d383b-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d383b-128">RELATED LINKS</span></span>

[<span data-ttu-id="d383b-129">Wyrejestrowanie — AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="d383b-129">Unregister-AzRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzRecoveryServicesBackupManagementServer.md)


