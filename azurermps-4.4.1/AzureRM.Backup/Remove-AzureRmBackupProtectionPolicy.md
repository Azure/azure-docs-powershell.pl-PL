---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 189E3DD8-AA43-4D4C-A873-971E0585E54E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 80b03c8ba4bab5968e55dff40633b014a586d450
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547079"
---
# <span data-ttu-id="58c67-101">Remove-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="58c67-101">Remove-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="58c67-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58c67-102">SYNOPSIS</span></span>
<span data-ttu-id="58c67-103">Usuwa zasadę z magazynu kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="58c67-103">Deletes a policy from a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58c67-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58c67-104">SYNTAX</span></span>

```
Remove-AzureRmBackupProtectionPolicy [-Force] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58c67-105">Opis</span><span class="sxs-lookup"><span data-stu-id="58c67-105">DESCRIPTION</span></span>
<span data-ttu-id="58c67-106">Polecenie cmdlet **Remove-AzureRmBackupProtectionPolicy** usuwa zasady z magazynu kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="58c67-106">The **Remove-AzureRmBackupProtectionPolicy** cmdlet deletes a policy from an Azure Backup vault.</span></span>

<span data-ttu-id="58c67-107">Przed usunięciem zasad ochrony kopii zapasowej zasady nie mogą zawierać żadnych elementów kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="58c67-107">Before you can delete a backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="58c67-108">Przed usunięciem zasad upewnij się, że każdy skojarzony element jest skojarzony z innymi zasadami.</span><span class="sxs-lookup"><span data-stu-id="58c67-108">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="58c67-109">Aby skojarzyć inne zasady z elementem kopii zapasowej, użyj polecenia cmdlet Enable-AzureRmBackupProtection.</span><span class="sxs-lookup"><span data-stu-id="58c67-109">To associate another policy with a backup item, use the Enable-AzureRmBackupProtection cmdlet.</span></span>

## <span data-ttu-id="58c67-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58c67-110">EXAMPLES</span></span>

### <span data-ttu-id="58c67-111">Przykład 1: usuwanie zasad ochrony kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="58c67-111">Example 1: Remove a backup protection policy</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DailyBackup" | Remove-AzureRmBackupProtectionPolicy
```

<span data-ttu-id="58c67-112">Pierwsze polecenie uzyskuje magazyn o nazwie Vault03 przy użyciu polecenia cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="58c67-112">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="58c67-113">Polecenie zapisuje ten obiekt w zmiennej $Vault.</span><span class="sxs-lookup"><span data-stu-id="58c67-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="58c67-114">Drugie polecenie tworzy zasady przechowywania przez 30 dni codziennego przechowywania, a następnie zapisuje je w zmiennej $Daily.</span><span class="sxs-lookup"><span data-stu-id="58c67-114">The second command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>

<span data-ttu-id="58c67-115">Drugie polecenie pobiera zasady ochrony o nazwie DailyBackup w magazynie w $Vault przy użyciu polecenia cmdlet **Get-AzureRmBackupProtectionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="58c67-115">The second command gets the protection policy named DailyBackup in the vault in $Vault by using the **Get-AzureRmBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="58c67-116">Polecenie przekazuje zasady do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58c67-116">The command passes the policy to the current cmdlet.</span></span>
<span data-ttu-id="58c67-117">To polecenie cmdlet usuwa zasady.</span><span class="sxs-lookup"><span data-stu-id="58c67-117">That cmdlet removes the policy.</span></span>

## <span data-ttu-id="58c67-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58c67-118">PARAMETERS</span></span>

### <span data-ttu-id="58c67-119">-Force</span><span class="sxs-lookup"><span data-stu-id="58c67-119">-Force</span></span>
<span data-ttu-id="58c67-120">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="58c67-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="58c67-121">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="58c67-121">-ProtectionPolicy</span></span>
<span data-ttu-id="58c67-122">Określa zasady ochrony, które usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58c67-122">Specifies protection policy that this cmdlet removes.</span></span>
<span data-ttu-id="58c67-123">Aby uzyskać **AzureRmBackupProtectionPolicy** , użyj polecenia cmdlet Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="58c67-123">To obtain an **AzureRmBackupProtectionPolicy** , use the Get-AzureRmBackupProtectionPolicy cmdlet</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58c67-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="58c67-124">-Confirm</span></span>
<span data-ttu-id="58c67-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58c67-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58c67-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58c67-126">-WhatIf</span></span>
<span data-ttu-id="58c67-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58c67-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58c67-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="58c67-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58c67-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58c67-129">-DefaultProfile</span></span>
<span data-ttu-id="58c67-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="58c67-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58c67-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58c67-131">CommonParameters</span></span>
<span data-ttu-id="58c67-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58c67-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58c67-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58c67-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58c67-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58c67-134">INPUTS</span></span>

### <span data-ttu-id="58c67-135">AzureRMBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="58c67-135">AzureRMBackupProtectionPolicy</span></span>

## <span data-ttu-id="58c67-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58c67-136">OUTPUTS</span></span>

### <span data-ttu-id="58c67-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="58c67-137">None</span></span>

## <span data-ttu-id="58c67-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58c67-138">NOTES</span></span>

## <span data-ttu-id="58c67-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58c67-139">RELATED LINKS</span></span>

[<span data-ttu-id="58c67-140">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="58c67-140">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="58c67-141">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="58c67-141">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="58c67-142">Nowe — AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="58c67-142">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


