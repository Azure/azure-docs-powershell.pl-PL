---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: A10DC2A2-A732-416F-9C68-6533C143AE8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: c5ab79ca42096ab93102be1288c772cab1ac01f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718132"
---
# <span data-ttu-id="bb716-101">Unregister-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="bb716-101">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="bb716-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bb716-102">SYNOPSIS</span></span>
<span data-ttu-id="bb716-103">Wyrejestrowuje serwer z systemem Windows lub inny kontener z magazynu.</span><span class="sxs-lookup"><span data-stu-id="bb716-103">Unregisters a Windows Server or other container from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb716-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bb716-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb716-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bb716-105">DESCRIPTION</span></span>
<span data-ttu-id="bb716-106">Polecenie cmdlet **Wyrejestrowanie — AzureRmRecoveryServicesBackupContainer** wyrejestruje system Windows Server lub inny kontener kopii zapasowych z magazynu.</span><span class="sxs-lookup"><span data-stu-id="bb716-106">The **Unregister-AzureRmRecoveryServicesBackupContainer** cmdlet unregisters a Windows Server or other Backup container from the vault.</span></span>
<span data-ttu-id="bb716-107">To polecenie cmdlet usuwa odwołania do kontenera z magazynu.</span><span class="sxs-lookup"><span data-stu-id="bb716-107">This cmdlet removes references to a container from the vault.</span></span>
<span data-ttu-id="bb716-108">Przed wyrejestrowaniem kontenera musisz usunąć wszelkie chronione dane skojarzone z tym kontenerem.</span><span class="sxs-lookup"><span data-stu-id="bb716-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

<span data-ttu-id="bb716-109">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="bb716-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="bb716-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bb716-110">EXAMPLES</span></span>

### <span data-ttu-id="bb716-111">Przykład 1: Wyrejestrowanie serwera Windows z magazynu</span><span class="sxs-lookup"><span data-stu-id="bb716-111">Example 1: Unregister a Windows Server from the vault</span></span>
```
PS C:\>$Cont = Get-AzureRmRecoveryServicesContainer -ContainerType "Windows" -BackupManagementType MARS -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupContainer -Container $Cont
```

<span data-ttu-id="bb716-112">Pierwsze polecenie uzyskuje kontener systemu Windows o nazwie server01.contoso.com zarejestrowany w magazynie, a następnie zapisuje go w zmiennej $Cont.</span><span class="sxs-lookup"><span data-stu-id="bb716-112">The first command gets the Windows container named server01.contoso.com that is registered in the vault, and then stores it in the $Cont variable.</span></span>

<span data-ttu-id="bb716-113">Drugie polecenie wyrejestrowuje określony serwer z magazynu kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bb716-113">The second command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

## <span data-ttu-id="bb716-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb716-114">PARAMETERS</span></span>

### <span data-ttu-id="bb716-115">-Kontener</span><span class="sxs-lookup"><span data-stu-id="bb716-115">-Container</span></span>
<span data-ttu-id="bb716-116">Określa obiekt kontenera kopii zapasowych do wyrejestrowania.</span><span class="sxs-lookup"><span data-stu-id="bb716-116">Specifies a Backup container object to unregister.</span></span>
<span data-ttu-id="bb716-117">Aby uzyskać obiekt **BackupContainer** , użyj polecenia cmdlet Get-AzureRmRecoveryServicesBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="bb716-117">To obtain a **BackupContainer** object, use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb716-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb716-118">-DefaultProfile</span></span>
<span data-ttu-id="bb716-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb716-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb716-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb716-120">CommonParameters</span></span>
<span data-ttu-id="bb716-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb716-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb716-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb716-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb716-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb716-123">INPUTS</span></span>

## <span data-ttu-id="bb716-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bb716-124">OUTPUTS</span></span>

## <span data-ttu-id="bb716-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bb716-125">NOTES</span></span>

## <span data-ttu-id="bb716-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb716-126">RELATED LINKS</span></span>

[<span data-ttu-id="bb716-127">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="bb716-127">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)


