---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 6602f1005877d4e38546338fd44d8fc51991a7b6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233954"
---
# <span data-ttu-id="0f7ed-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="0f7ed-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="0f7ed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0f7ed-102">SYNOPSIS</span></span>
<span data-ttu-id="0f7ed-103">Zwraca właściwości magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="0f7ed-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="0f7ed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0f7ed-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0f7ed-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0f7ed-105">DESCRIPTION</span></span>
<span data-ttu-id="0f7ed-106">Polecenie cmdlet **Get-AzRecoveryServicesVaultProperty** zwraca właściwości magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="0f7ed-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="0f7ed-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0f7ed-107">EXAMPLES</span></span>

### <span data-ttu-id="0f7ed-108">Przykład 1: pobieranie właściwości magazynu</span><span class="sxs-lookup"><span data-stu-id="0f7ed-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
```

<span data-ttu-id="0f7ed-109">Pierwsze polecenie pobiera obiekt magazynu, a następnie zapisuje go w zmiennej $vault.</span><span class="sxs-lookup"><span data-stu-id="0f7ed-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="0f7ed-110">Drugie polecenie pobiera właściwości magazynu.</span><span class="sxs-lookup"><span data-stu-id="0f7ed-110">The second command Gets the Vault Properties.</span></span>

## <span data-ttu-id="0f7ed-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0f7ed-111">PARAMETERS</span></span>

### <span data-ttu-id="0f7ed-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f7ed-112">-DefaultProfile</span></span>
<span data-ttu-id="0f7ed-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0f7ed-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f7ed-114">-VaultId</span><span class="sxs-lookup"><span data-stu-id="0f7ed-114">-VaultId</span></span>
<span data-ttu-id="0f7ed-115">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="0f7ed-115">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0f7ed-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f7ed-116">CommonParameters</span></span>
<span data-ttu-id="0f7ed-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f7ed-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f7ed-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f7ed-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f7ed-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f7ed-119">INPUTS</span></span>

### <span data-ttu-id="0f7ed-120">System. String</span><span class="sxs-lookup"><span data-stu-id="0f7ed-120">System.String</span></span>

## <span data-ttu-id="0f7ed-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0f7ed-121">OUTPUTS</span></span>

### <span data-ttu-id="0f7ed-122">Microsoft. Azure. Management. RecoveryServices. Backup. models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="0f7ed-122">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="0f7ed-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0f7ed-123">NOTES</span></span>

## <span data-ttu-id="0f7ed-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f7ed-124">RELATED LINKS</span></span>

[<span data-ttu-id="0f7ed-125">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="0f7ed-125">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="0f7ed-126">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="0f7ed-126">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)
