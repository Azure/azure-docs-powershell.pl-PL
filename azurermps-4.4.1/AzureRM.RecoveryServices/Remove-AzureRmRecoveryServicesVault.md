---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: b3df84865d29bbcf62074c1b1ed7f5586fb64fee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718110"
---
# <span data-ttu-id="597ee-101">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="597ee-101">Remove-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="597ee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="597ee-102">SYNOPSIS</span></span>
<span data-ttu-id="597ee-103">Usuwa magazyn usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="597ee-103">Deletes a Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="597ee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="597ee-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="597ee-105">Opis</span><span class="sxs-lookup"><span data-stu-id="597ee-105">DESCRIPTION</span></span>
<span data-ttu-id="597ee-106">Polecenie cmdlet **Remove-AzureRmRecoveryServicesVault** usuwa magazyn usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="597ee-106">The **Remove-AzureRmRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="597ee-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="597ee-107">EXAMPLES</span></span>

## <span data-ttu-id="597ee-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="597ee-108">PARAMETERS</span></span>

### <span data-ttu-id="597ee-109">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="597ee-109">-Vault</span></span>
<span data-ttu-id="597ee-110">Określa obiekt magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="597ee-110">Specifies an Azure Site Recovery vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="597ee-111">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="597ee-111">-Confirm</span></span>
<span data-ttu-id="597ee-112">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="597ee-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="597ee-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="597ee-113">-WhatIf</span></span>
<span data-ttu-id="597ee-114">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="597ee-114">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="597ee-115">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="597ee-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="597ee-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="597ee-116">-DefaultProfile</span></span>
<span data-ttu-id="597ee-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="597ee-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="597ee-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="597ee-118">CommonParameters</span></span>
<span data-ttu-id="597ee-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="597ee-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="597ee-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="597ee-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="597ee-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="597ee-121">INPUTS</span></span>

### <span data-ttu-id="597ee-122">ARSVault</span><span class="sxs-lookup"><span data-stu-id="597ee-122">ARSVault</span></span>
<span data-ttu-id="597ee-123">Parametr "magazyn" akceptuje wartość typu "ARSVault" z potoku.</span><span class="sxs-lookup"><span data-stu-id="597ee-123">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="597ee-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="597ee-124">OUTPUTS</span></span>

### <span data-ttu-id="597ee-125">Microsoft. Azure. Commands. RecoveryServices. VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="597ee-125">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="597ee-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="597ee-126">NOTES</span></span>

## <span data-ttu-id="597ee-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="597ee-127">RELATED LINKS</span></span>

[<span data-ttu-id="597ee-128">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="597ee-128">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="597ee-129">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="597ee-129">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="597ee-130">Nowe — AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="597ee-130">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)


