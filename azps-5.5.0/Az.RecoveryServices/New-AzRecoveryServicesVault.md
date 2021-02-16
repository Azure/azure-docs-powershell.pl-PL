---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
ms.openlocfilehash: 3bb602d148b0843def129a1e4538d9ef8fdbe169
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189291"
---
# <span data-ttu-id="0eb40-101">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="0eb40-101">New-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="0eb40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0eb40-102">SYNOPSIS</span></span>
<span data-ttu-id="0eb40-103">Tworzy nowy magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="0eb40-103">Creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="0eb40-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0eb40-104">SYNTAX</span></span>

```
New-AzRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0eb40-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0eb40-105">DESCRIPTION</span></span>
<span data-ttu-id="0eb40-106">Polecenie **cmdlet New-AzRecoveryServicesVault** tworzy nowy magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="0eb40-106">The **New-AzRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="0eb40-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0eb40-107">EXAMPLES</span></span>

### <span data-ttu-id="0eb40-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0eb40-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="0eb40-109">Utwórz magazyn usługi odzyskiwania w grupie zasobów i podanej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="0eb40-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="0eb40-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0eb40-110">PARAMETERS</span></span>

### <span data-ttu-id="0eb40-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eb40-111">-DefaultProfile</span></span>
<span data-ttu-id="0eb40-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0eb40-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0eb40-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0eb40-113">-Location</span></span>
<span data-ttu-id="0eb40-114">Określa nazwę lokalizacji geograficznej magazynu.</span><span class="sxs-lookup"><span data-stu-id="0eb40-114">Specifies the name of the geographic location of the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb40-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0eb40-115">-Name</span></span>
<span data-ttu-id="0eb40-116">Określa nazwę magazynu do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="0eb40-116">Specifies the name of the vault to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb40-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eb40-117">-ResourceGroupName</span></span>
<span data-ttu-id="0eb40-118">Określa nazwę grupy zasobów platformy Azure, w której chcesz utworzyć lub z której pobrać określony obiekt Usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="0eb40-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb40-119">— Tag</span><span class="sxs-lookup"><span data-stu-id="0eb40-119">-Tag</span></span>

<span data-ttu-id="0eb40-120">Określa tagi do dodania do magazynu usług odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="0eb40-120">Specifies the Tags to add to the Recovery Services Vault</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb40-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0eb40-121">-Confirm</span></span>
<span data-ttu-id="0eb40-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0eb40-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eb40-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eb40-123">-WhatIf</span></span>
<span data-ttu-id="0eb40-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0eb40-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0eb40-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0eb40-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eb40-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eb40-126">CommonParameters</span></span>
<span data-ttu-id="0eb40-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eb40-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eb40-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0eb40-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eb40-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0eb40-129">INPUTS</span></span>

### <span data-ttu-id="0eb40-130">Brak</span><span class="sxs-lookup"><span data-stu-id="0eb40-130">None</span></span>

## <span data-ttu-id="0eb40-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0eb40-131">OUTPUTS</span></span>

### <span data-ttu-id="0eb40-132">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="0eb40-132">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="0eb40-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0eb40-133">NOTES</span></span>

## <span data-ttu-id="0eb40-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0eb40-134">RELATED LINKS</span></span>

[<span data-ttu-id="0eb40-135">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="0eb40-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="0eb40-136">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="0eb40-136">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="0eb40-137">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="0eb40-137">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


