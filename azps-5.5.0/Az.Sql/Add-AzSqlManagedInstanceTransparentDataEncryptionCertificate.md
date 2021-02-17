---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
ms.openlocfilehash: e26d8aa68fd7ffcbab45073b845352feae83aea5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178538"
---
# <span data-ttu-id="0c4d6-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="0c4d6-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="0c4d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c4d6-102">SYNOPSIS</span></span>
<span data-ttu-id="0c4d6-103">Dodaje certyfikat przezroczystego szyfrowania danych dla danego zarządzanego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="0c4d6-103">Adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="0c4d6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0c4d6-104">SYNTAX</span></span>

```
Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ManagedInstanceName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c4d6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0c4d6-105">DESCRIPTION</span></span>
<span data-ttu-id="0c4d6-106">Ta Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate dodaje certyfikat przezroczystego szyfrowania danych dla danego zarządzanego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="0c4d6-106">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="0c4d6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0c4d6-107">EXAMPLES</span></span>

### <span data-ttu-id="0c4d6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0c4d6-108">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ManagedInstanceName "YourManagedInstanceName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

## <span data-ttu-id="0c4d6-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c4d6-109">PARAMETERS</span></span>

### <span data-ttu-id="0c4d6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c4d6-110">-DefaultProfile</span></span>
<span data-ttu-id="0c4d6-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c4d6-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c4d6-112">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="0c4d6-112">-ManagedInstanceName</span></span>
<span data-ttu-id="0c4d6-113">Nazwa zarządzanego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="0c4d6-113">The managed instance name</span></span>

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

### <span data-ttu-id="0c4d6-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c4d6-114">-PassThru</span></span>
<span data-ttu-id="0c4d6-115">Po pomyślnym wykonaniu zwraca dodany obiekt certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="0c4d6-115">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="0c4d6-116">— Hasło</span><span class="sxs-lookup"><span data-stu-id="0c4d6-116">-Password</span></span>
<span data-ttu-id="0c4d6-117">Hasło do certyfikatu przezroczystego szyfrowania danych</span><span class="sxs-lookup"><span data-stu-id="0c4d6-117">The Password for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c4d6-118">- PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="0c4d6-118">-PrivateBlob</span></span>
<span data-ttu-id="0c4d6-119">Prywatny obiekt blob dla certyfikatu szyfrowania przezroczystych danych</span><span class="sxs-lookup"><span data-stu-id="0c4d6-119">The Private blob for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c4d6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c4d6-120">-ResourceGroupName</span></span>
<span data-ttu-id="0c4d6-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0c4d6-121">The Resource Group Name</span></span>

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

### <span data-ttu-id="0c4d6-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0c4d6-122">-Confirm</span></span>
<span data-ttu-id="0c4d6-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0c4d6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c4d6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c4d6-124">-WhatIf</span></span>
<span data-ttu-id="0c4d6-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c4d6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c4d6-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0c4d6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c4d6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c4d6-127">CommonParameters</span></span>
<span data-ttu-id="0c4d6-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c4d6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c4d6-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c4d6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c4d6-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c4d6-130">INPUTS</span></span>

### <span data-ttu-id="0c4d6-131">Brak</span><span class="sxs-lookup"><span data-stu-id="0c4d6-131">None</span></span>

## <span data-ttu-id="0c4d6-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0c4d6-132">OUTPUTS</span></span>

### <span data-ttu-id="0c4d6-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0c4d6-133">System.Boolean</span></span>

## <span data-ttu-id="0c4d6-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0c4d6-134">NOTES</span></span>

## <span data-ttu-id="0c4d6-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c4d6-135">RELATED LINKS</span></span>
