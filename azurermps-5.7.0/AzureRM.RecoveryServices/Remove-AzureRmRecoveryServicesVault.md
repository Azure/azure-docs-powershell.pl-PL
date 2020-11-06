---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/remove-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: 4d3046827a7d3338833b0c8c788cfb7a9e18bc2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549599"
---
# <span data-ttu-id="8ce53-101">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="8ce53-101">Remove-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="8ce53-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8ce53-102">SYNOPSIS</span></span>
<span data-ttu-id="8ce53-103">Usuwa magazyn usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="8ce53-103">Deletes a Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ce53-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8ce53-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ce53-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8ce53-105">DESCRIPTION</span></span>
<span data-ttu-id="8ce53-106">Polecenie cmdlet **Remove-AzureRmRecoveryServicesVault** usuwa magazyn usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="8ce53-106">The **Remove-AzureRmRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="8ce53-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8ce53-107">EXAMPLES</span></span>

### <span data-ttu-id="8ce53-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8ce53-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="8ce53-109">Usuwa magazyn usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="8ce53-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="8ce53-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8ce53-110">PARAMETERS</span></span>

### <span data-ttu-id="8ce53-111">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="8ce53-111">-Vault</span></span>
<span data-ttu-id="8ce53-112">Określa obiekt magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8ce53-112">Specifies an Azure Site Recovery vault object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ce53-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8ce53-113">-Confirm</span></span>
<span data-ttu-id="8ce53-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ce53-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ce53-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ce53-115">-WhatIf</span></span>
<span data-ttu-id="8ce53-116">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ce53-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ce53-117">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8ce53-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ce53-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ce53-118">-DefaultProfile</span></span>
<span data-ttu-id="8ce53-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ce53-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ce53-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ce53-120">CommonParameters</span></span>
<span data-ttu-id="8ce53-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ce53-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ce53-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ce53-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ce53-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ce53-123">INPUTS</span></span>

### <span data-ttu-id="8ce53-124">ARSVault</span><span class="sxs-lookup"><span data-stu-id="8ce53-124">ARSVault</span></span>
<span data-ttu-id="8ce53-125">Parametr "magazyn" akceptuje wartość typu "ARSVault" z potoku.</span><span class="sxs-lookup"><span data-stu-id="8ce53-125">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="8ce53-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8ce53-126">OUTPUTS</span></span>

### <span data-ttu-id="8ce53-127">Microsoft. Azure. Commands. RecoveryServices. VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="8ce53-127">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="8ce53-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8ce53-128">NOTES</span></span>

## <span data-ttu-id="8ce53-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ce53-129">RELATED LINKS</span></span>

[<span data-ttu-id="8ce53-130">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="8ce53-130">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="8ce53-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="8ce53-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="8ce53-132">Nowe — AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="8ce53-132">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)


