---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
ms.openlocfilehash: 4e6dab95f110e25f24781b2ffbd01a016bdaa9fd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223211"
---
# <span data-ttu-id="6c473-101">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="6c473-101">Remove-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="6c473-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6c473-102">SYNOPSIS</span></span>
<span data-ttu-id="6c473-103">Usuwa magazyn usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="6c473-103">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="6c473-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6c473-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c473-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6c473-105">DESCRIPTION</span></span>
<span data-ttu-id="6c473-106">Polecenie cmdlet **Remove-AzRecoveryServicesVault** usuwa magazyn usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="6c473-106">The **Remove-AzRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="6c473-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6c473-107">EXAMPLES</span></span>

### <span data-ttu-id="6c473-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6c473-108">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="6c473-109">Usuwa magazyn usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="6c473-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="6c473-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6c473-110">PARAMETERS</span></span>

### <span data-ttu-id="6c473-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c473-111">-DefaultProfile</span></span>
<span data-ttu-id="6c473-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c473-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c473-113">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="6c473-113">-Vault</span></span>
<span data-ttu-id="6c473-114">Określa obiekt magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6c473-114">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="6c473-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6c473-115">-Confirm</span></span>
<span data-ttu-id="6c473-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c473-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c473-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c473-117">-WhatIf</span></span>
<span data-ttu-id="6c473-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c473-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c473-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6c473-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c473-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c473-120">CommonParameters</span></span>
<span data-ttu-id="6c473-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c473-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c473-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c473-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c473-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c473-123">INPUTS</span></span>

### <span data-ttu-id="6c473-124">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="6c473-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="6c473-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6c473-125">OUTPUTS</span></span>

### <span data-ttu-id="6c473-126">Microsoft. Azure. Commands. RecoveryServices. VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="6c473-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="6c473-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6c473-127">NOTES</span></span>

## <span data-ttu-id="6c473-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c473-128">RELATED LINKS</span></span>

[<span data-ttu-id="6c473-129">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="6c473-129">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="6c473-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="6c473-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="6c473-131">Nowe — AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="6c473-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)


