---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: c76bd152f64b337ca818c9e86b14fddbdaaf38cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553168"
---
# <span data-ttu-id="6b83a-101">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="6b83a-101">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="6b83a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6b83a-102">SYNOPSIS</span></span>
<span data-ttu-id="6b83a-103">Pobiera serwery usługi zarządzania zapasami SCDPM i Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="6b83a-103">Gets SCDPM and Azure Backup management servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b83a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6b83a-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupManagementServer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b83a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6b83a-105">DESCRIPTION</span></span>
<span data-ttu-id="6b83a-106">Polecenie cmdlet **Get-AzureRmRecoveryServicesBackupManagementServer** pobiera listę serwerów zarządzania zapasami, które są zarejestrowane w magazynie.</span><span class="sxs-lookup"><span data-stu-id="6b83a-106">The **Get-AzureRmRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>

<span data-ttu-id="6b83a-107">Istnieją dwa typy serwerów zarządzania kopiami zapasowymi: serwer System Center Data Protection Manager (SCDPM) i serwery zarządzania kopiami zapasowymi Azure.</span><span class="sxs-lookup"><span data-stu-id="6b83a-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="6b83a-108">Serwery zarządzania kopiami zapasowymi są instalowane osobno w celu zarządzania aranżacją kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="6b83a-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>

<span data-ttu-id="6b83a-109">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="6b83a-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="6b83a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6b83a-110">EXAMPLES</span></span>

### <span data-ttu-id="6b83a-111">Przykład 1: uzyskiwanie wszystkich serwerów zarządzania kopiami zapasowymi</span><span class="sxs-lookup"><span data-stu-id="6b83a-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupManagementServer
```

<span data-ttu-id="6b83a-112">To polecenie pobiera wszystkie serwery zarządzania zapasami zarejestrowane w magazynie.</span><span class="sxs-lookup"><span data-stu-id="6b83a-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="6b83a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6b83a-113">PARAMETERS</span></span>

### <span data-ttu-id="6b83a-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6b83a-114">-Name</span></span>
<span data-ttu-id="6b83a-115">Określa nazwę serwera zarządzania zapasami, którą należy uzyskać.</span><span class="sxs-lookup"><span data-stu-id="6b83a-115">Specifies the name of the Backup management server to get.</span></span>

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

### <span data-ttu-id="6b83a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b83a-116">-DefaultProfile</span></span>
<span data-ttu-id="6b83a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6b83a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b83a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b83a-118">CommonParameters</span></span>
<span data-ttu-id="6b83a-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b83a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b83a-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b83a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b83a-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b83a-121">INPUTS</span></span>

## <span data-ttu-id="6b83a-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6b83a-122">OUTPUTS</span></span>

### <span data-ttu-id="6b83a-123">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="6b83a-123">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

### <span data-ttu-id="6b83a-124">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. modele. BackupEngineBase]</span><span class="sxs-lookup"><span data-stu-id="6b83a-124">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase]</span></span>

## <span data-ttu-id="6b83a-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6b83a-125">NOTES</span></span>

## <span data-ttu-id="6b83a-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b83a-126">RELATED LINKS</span></span>

[<span data-ttu-id="6b83a-127">Wyrejestrowanie — AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="6b83a-127">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzureRmRecoveryServicesBackupManagementServer.md)


