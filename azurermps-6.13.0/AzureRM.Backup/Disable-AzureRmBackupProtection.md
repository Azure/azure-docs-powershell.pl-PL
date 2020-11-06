---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6E886340-864C-4FF6-8FA3-669D637770F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/disable-azurermbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
ms.openlocfilehash: ebea82628aae6df23d16a341f3fd503870a8037a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551400"
---
# <span data-ttu-id="69930-101">Disable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="69930-101">Disable-AzureRmBackupProtection</span></span>

## <span data-ttu-id="69930-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="69930-102">SYNOPSIS</span></span>
<span data-ttu-id="69930-103">Wyłącza ochronę elementu chronionego kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="69930-103">Disables protection for a Backup protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69930-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="69930-104">SYNTAX</span></span>

```
Disable-AzureRmBackupProtection [-RemoveRecoveryPoints] [-Force] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69930-105">Opis</span><span class="sxs-lookup"><span data-stu-id="69930-105">DESCRIPTION</span></span>
<span data-ttu-id="69930-106">Polecenie cmdlet **disable-AzureRmBackupProtection** wyłącza ochronę elementu chronionego za pomocą kopii zapasowej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="69930-106">The **Disable-AzureRmBackupProtection** cmdlet disables protection for an Azure Backup protected item.</span></span>
<span data-ttu-id="69930-107">To polecenie cmdlet zatrzymuje regularne Planowanie kopii zapasowej elementu.</span><span class="sxs-lookup"><span data-stu-id="69930-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="69930-108">To polecenie cmdlet umożliwia usunięcie istniejących punktów odzyskiwania dla elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="69930-108">This cmdlet can delete existing recovery points for the backup item.</span></span>

## <span data-ttu-id="69930-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="69930-109">EXAMPLES</span></span>

## <span data-ttu-id="69930-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="69930-110">PARAMETERS</span></span>

### <span data-ttu-id="69930-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69930-111">-DefaultProfile</span></span>
<span data-ttu-id="69930-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="69930-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69930-113">-Force</span><span class="sxs-lookup"><span data-stu-id="69930-113">-Force</span></span>
<span data-ttu-id="69930-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="69930-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="69930-115">-Item</span><span class="sxs-lookup"><span data-stu-id="69930-115">-Item</span></span>
<span data-ttu-id="69930-116">Określa element kopii zapasowej, dla którego to polecenie cmdlet wyłącza ochronę.</span><span class="sxs-lookup"><span data-stu-id="69930-116">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="69930-117">Aby uzyskać **AzureRmBackupItem** , użyj polecenia cmdlet Get-AzureRmBackupItem.</span><span class="sxs-lookup"><span data-stu-id="69930-117">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69930-118">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="69930-118">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="69930-119">Wskazuje, że to polecenie cmdlet usuwa istniejące punkty odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="69930-119">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="69930-120">Aby później usunąć zapisane punkty odzyskiwania, uruchom ponownie to polecenie cmdlet i określ ten parametr.</span><span class="sxs-lookup"><span data-stu-id="69930-120">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

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

### <span data-ttu-id="69930-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="69930-121">-Confirm</span></span>
<span data-ttu-id="69930-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69930-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69930-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69930-123">-WhatIf</span></span>
<span data-ttu-id="69930-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69930-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69930-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="69930-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69930-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69930-126">CommonParameters</span></span>
<span data-ttu-id="69930-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69930-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69930-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69930-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69930-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69930-129">INPUTS</span></span>

### <span data-ttu-id="69930-130">Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupItem</span><span class="sxs-lookup"><span data-stu-id="69930-130">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem</span></span>
<span data-ttu-id="69930-131">Parametry: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="69930-131">Parameters: Item (ByValue)</span></span>

## <span data-ttu-id="69930-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="69930-132">OUTPUTS</span></span>

### <span data-ttu-id="69930-133">Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="69930-133">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="69930-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="69930-134">NOTES</span></span>

## <span data-ttu-id="69930-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69930-135">RELATED LINKS</span></span>

[<span data-ttu-id="69930-136">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="69930-136">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="69930-137">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="69930-137">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)


