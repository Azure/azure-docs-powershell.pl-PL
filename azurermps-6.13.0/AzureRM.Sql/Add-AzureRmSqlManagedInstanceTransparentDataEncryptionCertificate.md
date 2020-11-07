---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.md
ms.openlocfilehash: 9fe8e36a752b4643ba44a59e8c44954bf25284c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717048"
---
# <span data-ttu-id="821ca-101">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="821ca-101">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="821ca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="821ca-102">SYNOPSIS</span></span>
<span data-ttu-id="821ca-103">Dodaje przezroczysty certyfikat szyfrowania danych dla danego wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="821ca-103">Adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="821ca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="821ca-104">SYNTAX</span></span>

```
Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ManagedInstanceName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="821ca-105">Opis</span><span class="sxs-lookup"><span data-stu-id="821ca-105">DESCRIPTION</span></span>
<span data-ttu-id="821ca-106">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate dodaje przezroczysty certyfikat szyfrowania danych dla danego wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="821ca-106">The Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="821ca-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="821ca-107">EXAMPLES</span></span>

### <span data-ttu-id="821ca-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="821ca-108">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ManagedInstanceName "YourManagedInstanceName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

## <span data-ttu-id="821ca-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="821ca-109">PARAMETERS</span></span>

### <span data-ttu-id="821ca-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="821ca-110">-DefaultProfile</span></span>
<span data-ttu-id="821ca-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="821ca-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="821ca-112">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="821ca-112">-ManagedInstanceName</span></span>
<span data-ttu-id="821ca-113">Nazwa zarządzanego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="821ca-113">The managed instance name</span></span>

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

### <span data-ttu-id="821ca-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="821ca-114">-PassThru</span></span>
<span data-ttu-id="821ca-115">Po poprawnym wykonaniu zostanie zwrócony obiekt certyfikatu, który został dodany.</span><span class="sxs-lookup"><span data-stu-id="821ca-115">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="821ca-116">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="821ca-116">-Password</span></span>
<span data-ttu-id="821ca-117">Hasło dla przezroczystego certyfikatu szyfrowania danych</span><span class="sxs-lookup"><span data-stu-id="821ca-117">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="821ca-118">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="821ca-118">-PrivateBlob</span></span>
<span data-ttu-id="821ca-119">Prywatny obiekt BLOB dla przezroczystego certyfikatu szyfrowania danych</span><span class="sxs-lookup"><span data-stu-id="821ca-119">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="821ca-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="821ca-120">-ResourceGroupName</span></span>
<span data-ttu-id="821ca-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="821ca-121">The Resource Group Name</span></span>

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

### <span data-ttu-id="821ca-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="821ca-122">-Confirm</span></span>
<span data-ttu-id="821ca-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="821ca-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="821ca-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="821ca-124">-WhatIf</span></span>
<span data-ttu-id="821ca-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="821ca-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="821ca-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="821ca-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="821ca-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="821ca-127">CommonParameters</span></span>
<span data-ttu-id="821ca-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="821ca-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="821ca-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="821ca-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="821ca-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="821ca-130">INPUTS</span></span>

### <span data-ttu-id="821ca-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="821ca-131">None</span></span>

## <span data-ttu-id="821ca-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="821ca-132">OUTPUTS</span></span>

### <span data-ttu-id="821ca-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="821ca-133">System.Boolean</span></span>

## <span data-ttu-id="821ca-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="821ca-134">NOTES</span></span>

## <span data-ttu-id="821ca-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="821ca-135">RELATED LINKS</span></span>
