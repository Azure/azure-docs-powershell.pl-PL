---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 922BEA08-6619-4D4C-86EC-58279C9E1D93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/unregister-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
ms.openlocfilehash: 8c90137e142086d7ea7c0bcc34321b3f38a12d95
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541939"
---
# <span data-ttu-id="38776-101">Unregister-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="38776-101">Unregister-AzureRmBackupContainer</span></span>

## <span data-ttu-id="38776-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="38776-102">SYNOPSIS</span></span>
<span data-ttu-id="38776-103">Wyrejestrowuje kontener z magazynu kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="38776-103">Unregisters a container from a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38776-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="38776-104">SYNTAX</span></span>

```
Unregister-AzureRmBackupContainer [-Force] [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38776-105">Opis</span><span class="sxs-lookup"><span data-stu-id="38776-105">DESCRIPTION</span></span>
<span data-ttu-id="38776-106">Polecenie cmdlet **Unregister-AzureRmBackupContainer** umożliwia Wyrejestrowanie maszyny wirtualnej systemu Windows Server lub platformy Azure z magazynu kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="38776-106">The **Unregister-AzureRmBackupContainer** cmdlet unregisters the Windows Server or Azure virtual machine from an Azure Backup vault.</span></span>
<span data-ttu-id="38776-107">To polecenie cmdlet usuwa odwołania do kontenera z magazynu kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="38776-107">This cmdlet removes references to a container from the Backup vault.</span></span>
<span data-ttu-id="38776-108">Przed wyrejestrowaniem kontenera musisz usunąć wszelkie chronione dane skojarzone z tym kontenerem.</span><span class="sxs-lookup"><span data-stu-id="38776-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

## <span data-ttu-id="38776-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="38776-109">EXAMPLES</span></span>

### <span data-ttu-id="38776-110">Przykład 1: Wyrejestrowanie systemu Windows Server</span><span class="sxs-lookup"><span data-stu-id="38776-110">Example 1: Unregister a Windows Server</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type Windows -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmBackupContainer -Container $Container[0]
Unregister Server
This operation will delete all data in the backup vault that is associated with the server. Are you sure you want to unregister the server? 
[] Yes  [] No  [?] Help (default is "No"): Yes
```

<span data-ttu-id="38776-111">Pierwsze polecenie uzyskuje magazyn o nazwie Vault03 przy użyciu polecenia cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="38776-111">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="38776-112">Polecenie zapisuje ten obiekt w zmiennej $Vault.</span><span class="sxs-lookup"><span data-stu-id="38776-112">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="38776-113">Drugie polecenie pobiera kontener o określonej nazwie w magazynie w $Vault przy użyciu Get-AzureRmBackupContainer polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38776-113">The second command gets a container that has the specified name in the vault in $Vault by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="38776-114">Polecenie zapisuje ten obiekt w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="38776-114">The command stores that object in the $Container variable.</span></span>
<span data-ttu-id="38776-115">Polecenie ostatnie wyrejestrowuje określony serwer z magazynu kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="38776-115">The final command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

### <span data-ttu-id="38776-116">Przykład 2: Wyrejestrowanie serwera Windows bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="38776-116">Example 2: Unregister a Windows Server without confirmation</span></span>
```
PS C:\>Unregister-AzureRmBackupContainer -Container $Container[0] -Force
```

<span data-ttu-id="38776-117">To polecenie wyrejestrowuje określony serwer z magazynu kopii zapasowych platformy Azure, tak jak w pierwszym przykładzie.</span><span class="sxs-lookup"><span data-stu-id="38776-117">This command unregisters the specified Windows Server from the Azure Backup vault, just as in the first example.</span></span>
<span data-ttu-id="38776-118">To polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="38776-118">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="38776-119">Dlatego polecenie nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="38776-119">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="38776-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="38776-120">PARAMETERS</span></span>

### <span data-ttu-id="38776-121">-Kontener</span><span class="sxs-lookup"><span data-stu-id="38776-121">-Container</span></span>
<span data-ttu-id="38776-122">Określa, że wyrejestruje się to polecenie cmdlet w systemie Windows Server lub maszynie wirtualnej Azure.</span><span class="sxs-lookup"><span data-stu-id="38776-122">Specifies the Windows Server or Azure virtual machine that this cmdlet unregisters.</span></span>
<span data-ttu-id="38776-123">Aby uzyskać **AzureRmBackupContainer** , użyj polecenia cmdlet Get-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="38776-123">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38776-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38776-124">-DefaultProfile</span></span>
<span data-ttu-id="38776-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="38776-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38776-126">-Force</span><span class="sxs-lookup"><span data-stu-id="38776-126">-Force</span></span>
<span data-ttu-id="38776-127">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="38776-127">Forces the command to run without asking for user confirmation.</span></span>
<span data-ttu-id="38776-128">Ten parametr dotyczy tylko obiektów **AzureBackupContainer** typu Windows.</span><span class="sxs-lookup"><span data-stu-id="38776-128">This parameter is relevant only for **AzureBackupContainer** objects of type Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38776-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="38776-129">-Confirm</span></span>
<span data-ttu-id="38776-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38776-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38776-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38776-131">-WhatIf</span></span>
<span data-ttu-id="38776-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38776-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38776-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="38776-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38776-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38776-134">CommonParameters</span></span>
<span data-ttu-id="38776-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38776-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38776-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38776-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38776-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38776-137">INPUTS</span></span>

### <span data-ttu-id="38776-138">Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupContainer</span><span class="sxs-lookup"><span data-stu-id="38776-138">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer</span></span>
<span data-ttu-id="38776-139">Parametry: kontener (ByValue)</span><span class="sxs-lookup"><span data-stu-id="38776-139">Parameters: Container (ByValue)</span></span>

## <span data-ttu-id="38776-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="38776-140">OUTPUTS</span></span>

### <span data-ttu-id="38776-141">Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="38776-141">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="38776-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="38776-142">NOTES</span></span>
* <span data-ttu-id="38776-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="38776-143">None</span></span>

## <span data-ttu-id="38776-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38776-144">RELATED LINKS</span></span>

[<span data-ttu-id="38776-145">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="38776-145">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="38776-146">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="38776-146">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="38776-147">Rejestr — AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="38776-147">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)


