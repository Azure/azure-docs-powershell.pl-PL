---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A10DC2A2-A732-416F-9C68-6533C143AE8F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/unregister-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 0da09971892c03c157d9679da8feb88bdd66a73f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050576"
---
# <span data-ttu-id="3a7fa-101">Unregister-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="3a7fa-101">Unregister-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="3a7fa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a7fa-102">SYNOPSIS</span></span>
<span data-ttu-id="3a7fa-103">Wyrejestrowuje serwer z systemem Windows lub inny kontener z magazynu.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-103">Unregisters a Windows Server or other container from the vault.</span></span>

## <span data-ttu-id="3a7fa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a7fa-104">SYNTAX</span></span>

```
Unregister-AzRecoveryServicesBackupContainer [-Container] <ContainerBase> [-PassThru] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a7fa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3a7fa-105">DESCRIPTION</span></span>
<span data-ttu-id="3a7fa-106">Polecenie cmdlet **Wyrejestrowanie — AzRecoveryServicesBackupContainer** wyrejestruje system Windows Server lub inny kontener kopii zapasowych z magazynu.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-106">The **Unregister-AzRecoveryServicesBackupContainer** cmdlet unregisters a Windows Server or other Backup container from the vault.</span></span>
<span data-ttu-id="3a7fa-107">To polecenie cmdlet usuwa odwołania do kontenera z magazynu.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-107">This cmdlet removes references to a container from the vault.</span></span>
<span data-ttu-id="3a7fa-108">Przed wyrejestrowaniem kontenera musisz usunąć wszelkie chronione dane skojarzone z tym kontenerem.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="3a7fa-109">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="3a7fa-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a7fa-110">EXAMPLES</span></span>

### <span data-ttu-id="3a7fa-111">Przykład 1: Wyrejestrowanie serwera Windows z magazynu</span><span class="sxs-lookup"><span data-stu-id="3a7fa-111">Example 1: Unregister a Windows Server from the vault</span></span>
```
PS C:\>$Cont = Get-AzRecoveryServicesBackupContainer -ContainerType "Windows" -BackupManagementType MARS -Name "server01.contoso.com"
PS C:\> Unregister-AzRecoveryServicesBackupContainer -Container $Cont
```

<span data-ttu-id="3a7fa-112">Pierwsze polecenie uzyskuje kontener systemu Windows o nazwie server01.contoso.com zarejestrowany w magazynie, a następnie zapisuje go w zmiennej $Cont.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-112">The first command gets the Windows container named server01.contoso.com that is registered in the vault, and then stores it in the $Cont variable.</span></span>
<span data-ttu-id="3a7fa-113">Drugie polecenie wyrejestrowuje określony serwer z magazynu kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-113">The second command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

## <span data-ttu-id="3a7fa-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a7fa-114">PARAMETERS</span></span>

### <span data-ttu-id="3a7fa-115">-Kontener</span><span class="sxs-lookup"><span data-stu-id="3a7fa-115">-Container</span></span>
<span data-ttu-id="3a7fa-116">Określa obiekt kontenera kopii zapasowych do wyrejestrowania.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-116">Specifies a Backup container object to unregister.</span></span>
<span data-ttu-id="3a7fa-117">Aby uzyskać obiekt **BackupContainer** , użyj polecenia cmdlet Get-AzRecoveryServicesBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-117">To obtain a **BackupContainer** object, use the Get-AzRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a7fa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a7fa-118">-DefaultProfile</span></span>
<span data-ttu-id="3a7fa-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a7fa-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a7fa-120">-PassThru</span></span>
<span data-ttu-id="3a7fa-121">Zwraca kontener, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-121">Return the container to be deleted.</span></span>

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

### <span data-ttu-id="3a7fa-122">-VaultId</span><span class="sxs-lookup"><span data-stu-id="3a7fa-122">-VaultId</span></span>
<span data-ttu-id="3a7fa-123">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-123">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="3a7fa-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3a7fa-124">-Confirm</span></span>
<span data-ttu-id="3a7fa-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a7fa-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a7fa-126">-WhatIf</span></span>
<span data-ttu-id="3a7fa-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a7fa-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a7fa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a7fa-129">CommonParameters</span></span>
<span data-ttu-id="3a7fa-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a7fa-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a7fa-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a7fa-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a7fa-132">INPUTS</span></span>

### <span data-ttu-id="3a7fa-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3a7fa-133">System.String</span></span>

## <span data-ttu-id="3a7fa-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a7fa-134">OUTPUTS</span></span>

### <span data-ttu-id="3a7fa-135">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="3a7fa-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="3a7fa-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a7fa-136">NOTES</span></span>

## <span data-ttu-id="3a7fa-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a7fa-137">RELATED LINKS</span></span>

[<span data-ttu-id="3a7fa-138">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="3a7fa-138">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)


