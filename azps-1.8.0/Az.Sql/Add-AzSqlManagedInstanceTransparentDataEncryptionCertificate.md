---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
ms.openlocfilehash: dc73939aaae76c0444307cbd1aa6bfb08711b2e9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708049"
---
# <span data-ttu-id="b0457-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="b0457-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="b0457-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b0457-102">SYNOPSIS</span></span>
<span data-ttu-id="b0457-103">Dodaje przezroczysty certyfikat szyfrowania danych dla danego wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="b0457-103">Adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="b0457-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b0457-104">SYNTAX</span></span>

```
Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ManagedInstanceName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0457-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b0457-105">DESCRIPTION</span></span>
<span data-ttu-id="b0457-106">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate dodaje przezroczysty certyfikat szyfrowania danych dla danego wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="b0457-106">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="b0457-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b0457-107">EXAMPLES</span></span>

### <span data-ttu-id="b0457-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b0457-108">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ManagedInstanceName "YourManagedInstanceName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

## <span data-ttu-id="b0457-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b0457-109">PARAMETERS</span></span>

### <span data-ttu-id="b0457-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0457-110">-DefaultProfile</span></span>
<span data-ttu-id="b0457-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b0457-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0457-112">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="b0457-112">-ManagedInstanceName</span></span>
<span data-ttu-id="b0457-113">Nazwa zarządzanego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="b0457-113">The managed instance name</span></span>

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

### <span data-ttu-id="b0457-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0457-114">-PassThru</span></span>
<span data-ttu-id="b0457-115">Po poprawnym wykonaniu zostanie zwrócony obiekt certyfikatu, który został dodany.</span><span class="sxs-lookup"><span data-stu-id="b0457-115">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="b0457-116">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="b0457-116">-Password</span></span>
<span data-ttu-id="b0457-117">Hasło dla przezroczystego certyfikatu szyfrowania danych</span><span class="sxs-lookup"><span data-stu-id="b0457-117">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="b0457-118">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="b0457-118">-PrivateBlob</span></span>
<span data-ttu-id="b0457-119">Prywatny obiekt BLOB dla przezroczystego certyfikatu szyfrowania danych</span><span class="sxs-lookup"><span data-stu-id="b0457-119">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="b0457-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0457-120">-ResourceGroupName</span></span>
<span data-ttu-id="b0457-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b0457-121">The Resource Group Name</span></span>

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

### <span data-ttu-id="b0457-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b0457-122">-Confirm</span></span>
<span data-ttu-id="b0457-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0457-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0457-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0457-124">-WhatIf</span></span>
<span data-ttu-id="b0457-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0457-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0457-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b0457-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0457-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0457-127">CommonParameters</span></span>
<span data-ttu-id="b0457-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0457-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0457-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0457-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0457-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0457-130">INPUTS</span></span>

### <span data-ttu-id="b0457-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b0457-131">None</span></span>

## <span data-ttu-id="b0457-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b0457-132">OUTPUTS</span></span>

### <span data-ttu-id="b0457-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b0457-133">System.Boolean</span></span>

## <span data-ttu-id="b0457-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b0457-134">NOTES</span></span>

## <span data-ttu-id="b0457-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0457-135">RELATED LINKS</span></span>
