---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/import-AzWebAppKeyVaultCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Import-AzWebAppKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Import-AzWebAppKeyVaultCertificate.md
ms.openlocfilehash: d92aa19573a238d7f54a21f7888bbd93ac07107b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007418"
---
# <span data-ttu-id="15bee-101">Import-AzWebAppKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="15bee-101">Import-AzWebAppKeyVaultCertificate</span></span>

## <span data-ttu-id="15bee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15bee-102">SYNOPSIS</span></span>
<span data-ttu-id="15bee-103">Importowanie certyfikatu SSL do aplikacji sieci Web z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="15bee-103">Import an SSL certificate to a web app from Key Vault.</span></span>

## <span data-ttu-id="15bee-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="15bee-104">SYNTAX</span></span>

```
Import-AzWebAppKeyVaultCertificate [-KeyVaultName] <String> [-CertName] <String> [-ResourceGroupName] <String>
 [-WebAppName] <String> [-Slot <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15bee-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="15bee-105">DESCRIPTION</span></span>
<span data-ttu-id="15bee-106">Polecenie **cmdlet Import-AzWebAppKeyVaultCertificate** importuje certyfikat SSL do aplikacji sieci Web z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="15bee-106">The **Import-AzWebAppKeyVaultCertificate** cmdlet imports an SSL certificate to a web app from Key Vault.</span></span>

## <span data-ttu-id="15bee-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="15bee-107">EXAMPLES</span></span>

### <span data-ttu-id="15bee-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="15bee-108">Example 1</span></span>
```powershell
PS C:\> Import-AzWebAppKeyVaultCertificate -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" 
-KeyVaultName "ContosoKeyVault" -CertName "ContosoCertname"
```

<span data-ttu-id="15bee-109">To polecenie importuje certyfikat SSL do aplikacji sieci Web z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="15bee-109">This command imports an SSL certificate to a web app from Key Vault.</span></span>

### <span data-ttu-id="15bee-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="15bee-110">Example 2</span></span>
```powershell
PS C:\> Import-AzWebAppKeyVaultCertificate -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" 
-KeyVaultName  '/subscriptions/[sub id]/resourceGroups/[rg]/providers/Microsoft.KeyVault/vaults/[vault name]' 
-CertName "ContosoCertname"
```

<span data-ttu-id="15bee-111">To polecenie Importuj certyfikat SSL do aplikacji sieci Web z magazynu kluczy przy użyciu identyfikatora zasobu (zwykle jeśli magazyn kluczy znajduje się w innej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="15bee-111">This command Import an SSL certificate to a web app from Key Vault using resource id (typically if Key Vault is in another subscription).</span></span>

## <span data-ttu-id="15bee-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15bee-112">PARAMETERS</span></span>

### <span data-ttu-id="15bee-113">-CertName</span><span class="sxs-lookup"><span data-stu-id="15bee-113">-CertName</span></span>
<span data-ttu-id="15bee-114">KeyVaultCertName certyfikatu utworzonego w keyvault</span><span class="sxs-lookup"><span data-stu-id="15bee-114">KeyVaultCertName of the certificate created in keyvault</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15bee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15bee-115">-DefaultProfile</span></span>
<span data-ttu-id="15bee-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="15bee-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15bee-117">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="15bee-117">-KeyVaultName</span></span>
<span data-ttu-id="15bee-118">Nazwa keyvault.</span><span class="sxs-lookup"><span data-stu-id="15bee-118">The name of the keyvault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15bee-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15bee-119">-ResourceGroupName</span></span>
<span data-ttu-id="15bee-120">Nazwa grupy zasobów aplikacji WebApp.</span><span class="sxs-lookup"><span data-stu-id="15bee-120">The name of the webapp resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15bee-121">— Slot</span><span class="sxs-lookup"><span data-stu-id="15bee-121">-Slot</span></span>
<span data-ttu-id="15bee-122">Nazwa gniazda aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="15bee-122">The name of the webapp slot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15bee-123">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="15bee-123">-WebAppName</span></span>
<span data-ttu-id="15bee-124">Nazwa aplikacji webapp.</span><span class="sxs-lookup"><span data-stu-id="15bee-124">The name of the webapp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15bee-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="15bee-125">-Confirm</span></span>
<span data-ttu-id="15bee-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="15bee-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15bee-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15bee-127">-WhatIf</span></span>
<span data-ttu-id="15bee-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15bee-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15bee-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="15bee-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15bee-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15bee-130">CommonParameters</span></span>
<span data-ttu-id="15bee-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15bee-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15bee-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15bee-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15bee-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15bee-133">INPUTS</span></span>

### <span data-ttu-id="15bee-134">Brak</span><span class="sxs-lookup"><span data-stu-id="15bee-134">None</span></span>

## <span data-ttu-id="15bee-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15bee-135">OUTPUTS</span></span>

### <span data-ttu-id="15bee-136">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="15bee-136">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="15bee-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="15bee-137">NOTES</span></span>

## <span data-ttu-id="15bee-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="15bee-138">RELATED LINKS</span></span>
