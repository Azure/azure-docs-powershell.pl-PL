---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 698DCD00-13C0-4C36-A74B-35215D608339
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
ms.openlocfilehash: 8530dbff2e348f1b068afe7293cae9c993ce064e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547071"
---
# <span data-ttu-id="4ef04-101">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="4ef04-101">Remove-AzureRmBackupVault</span></span>

## <span data-ttu-id="4ef04-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4ef04-102">SYNOPSIS</span></span>
<span data-ttu-id="4ef04-103">Usuwa magazyn kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="4ef04-103">Deletes a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ef04-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4ef04-104">SYNTAX</span></span>

```
Remove-AzureRmBackupVault [-Force] [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ef04-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4ef04-105">DESCRIPTION</span></span>
<span data-ttu-id="4ef04-106">Polecenie cmdlet **Remove-AzureRmBackupVault** usuwa magazyn kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4ef04-106">The **Remove-AzureRmBackupVault** cmdlet deletes an Azure Backup vault.</span></span>

<span data-ttu-id="4ef04-107">Aby można było usunąć magazyn kopii zapasowych, musi on być pusty.</span><span class="sxs-lookup"><span data-stu-id="4ef04-107">Before you can delete a Backup vault, it must be empty.</span></span>
<span data-ttu-id="4ef04-108">Użyj polecenia cmdlet **Remove-AzureRmBackupContainer** w celu usunięcia infrastruktury jako danych kopii zapasowej maszyny wirtualnej usługi (IaaS) z magazynu.</span><span class="sxs-lookup"><span data-stu-id="4ef04-108">Use the **Remove-AzureRmBackupContainer** cmdlet to remove infrastructure as a service (IaaS) virtual machine backup data from the vault.</span></span>
<span data-ttu-id="4ef04-109">Użyj polecenia cmdlet **delete-RegisteredServer** , aby usunąć inne zarejestrowane serwery i dane kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="4ef04-109">Use the **Delete-RegisteredServer** cmdlet to remove other registered servers and backup data.</span></span>

## <span data-ttu-id="4ef04-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4ef04-110">EXAMPLES</span></span>

### <span data-ttu-id="4ef04-111">Przykład 1: Usuwanie magazynu kopii zapasowych Azure</span><span class="sxs-lookup"><span data-stu-id="4ef04-111">Example 1: Delete an Azure Backup vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Remove-AzureRmBackupVault
```

<span data-ttu-id="4ef04-112">To polecenie pobiera magazyn kopii zapasowych Azure o nazwie Vault03 przy użyciu polecenia cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="4ef04-112">This command gets the Azure Backup vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="4ef04-113">Polecenie przekazuje ten magazyn do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="4ef04-113">The command passes that vault to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4ef04-114">Bieżące polecenie cmdlet usuwa magazyn.</span><span class="sxs-lookup"><span data-stu-id="4ef04-114">The current cmdlet removes the vault.</span></span>

## <span data-ttu-id="4ef04-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4ef04-115">PARAMETERS</span></span>

### <span data-ttu-id="4ef04-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4ef04-116">-Force</span></span>
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

### <span data-ttu-id="4ef04-117">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="4ef04-117">-Vault</span></span>
<span data-ttu-id="4ef04-118">Określa magazyn kopii zapasowych, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ef04-118">Specifies a Backup vault that this cmdlet removes.</span></span>
<span data-ttu-id="4ef04-119">Aby uzyskać **AzureRmBackupVault** , użyj polecenia cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="4ef04-119">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ef04-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4ef04-120">-Confirm</span></span>
<span data-ttu-id="4ef04-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ef04-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ef04-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ef04-122">-WhatIf</span></span>
<span data-ttu-id="4ef04-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ef04-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ef04-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4ef04-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ef04-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ef04-125">-DefaultProfile</span></span>
<span data-ttu-id="4ef04-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4ef04-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ef04-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ef04-127">CommonParameters</span></span>
<span data-ttu-id="4ef04-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ef04-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ef04-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ef04-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ef04-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ef04-130">INPUTS</span></span>

### <span data-ttu-id="4ef04-131">AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="4ef04-131">AzureRMBackupVault</span></span>

## <span data-ttu-id="4ef04-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4ef04-132">OUTPUTS</span></span>

### <span data-ttu-id="4ef04-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4ef04-133">None</span></span>

## <span data-ttu-id="4ef04-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4ef04-134">NOTES</span></span>
* <span data-ttu-id="4ef04-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4ef04-135">None</span></span>

## <span data-ttu-id="4ef04-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ef04-136">RELATED LINKS</span></span>

[<span data-ttu-id="4ef04-137">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="4ef04-137">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="4ef04-138">Nowe — AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="4ef04-138">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="4ef04-139">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="4ef04-139">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


